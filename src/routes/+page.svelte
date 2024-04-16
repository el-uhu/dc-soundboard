<script>
    import { Gallery, Button } from 'flowbite-svelte';
    const images = [
      { alt: 'eisvogel', src: 'voegel/eisvogel.jpg' },
      { alt: 'buntspecht', src: 'voegel/buntspecht.jpg' },
      { alt: 'graureiher', src: 'voegel/graureiher.jpg' },
      { alt: 'elster', src: 'voegel/elster.jpg' },
      { alt: 'stockente', src: 'voegel/stockente02.jpg' },
      { alt: 'storch', src: 'voegel/storch.jpg' },
      { alt: 'taube', src: 'voegel/taube04.jpg' },
      { alt: 'uhu', src: 'voegel/uhu.jpg' },
      { alt: 'neuntoeter', src: 'voegel/neuntoeter.jpg' },
      { alt: 'rotkehlchen', src: 'voegel/rotkehlchen.jpg' },
      { alt: 'schwan', src: 'voegel/schwan.jpg' },
      { alt: 'buntspecht', src: 'voegel/buntspecht.jpg' }
    ];
  </script>
  
  <div class="flex items-center justify-center py-4 md:py-8 flex-wrap gap-3 mb-3 mx-auto">
    <Button pill size="xl" outline>Alle</Button>
    <Button pill size="xl" color="alternative">Singvögel</Button>
    <Button pill size="xl" color="alternative">Raubvögel</Button>
    <Button pill size="xl" color="alternative">Wasservögel</Button>
  </div>
  
  <Gallery items={images} class="gap-4 grid-cols-2 md:grid-cols-4" />