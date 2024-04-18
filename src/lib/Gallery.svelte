<script lang="ts">
    import { Modal, Button, Heading, P, A, Secondary, Img } from 'flowbite-svelte'
    import { twMerge } from 'tailwind-merge';
    export let items
    export let imgClass: string = 'h-auto max-w-full rounded-lg';
  
    $: divClass = twMerge('grid', $$props.class);
  
    function init(node: HTMLElement) {
      if (getComputedStyle(node).gap === 'normal') node.style.gap = 'inherit';
    }

   let modals = {};
  </script>
  
  <div {...$$restProps} class={divClass} use:init>
    {#each items as item}
      <slot {item}>
        <div>
            <button on:click={() => (item.modal = true)}>
                <img 
                    src={item.src} 
                    alt={item.name} 
                    class={twMerge(imgClass, $$props.classImg)} />  
            </button>
        </div>
        <Modal title="" bind:open={item.modal} autoclose outsideclose>
            <Heading tag="h2" customSize="text-4xl font-extrabold ">
                {item.name}
                <Secondary class="ms-2">{item.scientific}</Secondary>
            </Heading>

            <Img src={item.src} size="max-w-md" alignment="mx-auto" alt={item.name} />
            
            <p class="text-base leading-relaxed text-gray-500 dark:text-gray-400">
                {item.text}
            </p>
            <div class="flex items-center justify-center">
                <iframe src='https://xeno-canto.org/{item.xenoCantoID}/embed' scrolling='no' frameborder='0' width='520px' height='220'></iframe>
            </div>
          </Modal>
      </slot>
    {:else}
      <slot item={items[0]} />
    {/each}
  </div>