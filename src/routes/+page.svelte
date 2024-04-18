<script>
    import Gallery from '$lib/Gallery.svelte'
    import { Button } from 'flowbite-svelte';
    const images = [
      { alt: 'eisvogel', src: 'voegel/eisvogel.jpg', "modal": false },
      { alt: 'buntspecht', src: 'voegel/buntspecht.jpg', "modal": false },
      { alt: 'graureiher', src: 'voegel/graureiher.jpg', "modal": false },
      { alt: 'elster', src: 'voegel/elster.jpg', "modal": false },
      { alt: 'stockente', src: 'voegel/stockente02.jpg' , "modal": false },
      { alt: 'storch', src: 'voegel/storch.jpg' , "modal": false },
      { alt: 'taube', src: 'voegel/taube04.jpg' , "modal": false },
      { alt: 'uhu', src: 'voegel/uhu.jpg' , "modal": false },
      { alt: 'neuntoeter', src: 'voegel/neuntoeter.jpg' , "modal": false },
      { alt: 'rotkehlchen', src: 'voegel/rotkehlchen.jpg' , "modal": false },
      { alt: 'schwan', src: 'voegel/schwan.jpg' , "modal": false },
      { alt: 'buntspecht', src: 'voegel/buntspecht.jpg', "modal": false }
    ];
  </script>
  
  <div class="flex items-center justify-center py-4 md:py-8 flex-wrap gap-3 mb-3 mx-auto">
    <Button pill size="xl" outline>Alle</Button>
    <Button pill size="xl" color="alternative">Singvögel</Button>
    <Button pill size="xl" color="alternative">Raubvögel</Button>
    <Button pill size="xl" color="alternative">Wasservögel</Button>
  </div>
  
  <Gallery items={images} class="gap-4 grid-cols-2 md:grid-cols-4" />