<script lang="ts">
    import { Modal, Button } from 'flowbite-svelte'
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
                <img src={item.src} alt={item.alt} class={twMerge(imgClass, $$props.classImg)} />  
            </button>
        </div>
        <Modal title={item.src} bind:open={item.modal} autoclose outsideclose>
            <p class="text-base leading-relaxed text-gray-500 dark:text-gray-400">With less than a month to go before the European Union enacts new consumer privacy laws for its citizens, companies around the world are updating their terms of service agreements to comply.</p>
          </Modal>
      </slot>
    {:else}
      <slot item={items[0]} />
    {/each}
  </div>