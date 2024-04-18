<script>
	import '../app.pcss';
	import { Navbar, NavBrand, NavLi, NavUl, NavHamburger, Footer, FooterBrand, FooterCopyright, FooterIcon, FooterLink, FooterLinkGroup } from 'flowbite-svelte';
	export const prerender = true;
</script>

<Navbar  >
	<NavBrand href="/">
	  <img src="warbler.png" class="me-3 h-6 sm:h-9" alt="Flowbite Logo" />
	  <span class="self-center whitespace-nowrap text-xl font-semibold dark:text-white">Dawn Chorus Soundboard</span>
	</NavBrand>
	<NavHamburger  />
	<NavUl >
	  <NavLi href="/">Home</NavLi>
	  <NavLi href="http://el-uhu.github.io/dawnchorus">About</NavLi>
	</NavUl>
</Navbar>

<div class="m-5">
	<slot></slot>

	<div class="p-9">
		<Footer>
			<FooterCopyright href="/" by="BG/BRG St. Martin Villach™" year={2024} />
			<!-- <FooterLinkGroup ulClass="flex flex-wrap items-center mt-3 text-sm text-gray-500 dark:text-gray-400 sm:mt-0">
				<FooterLink href="/">About</FooterLink>
				<FooterLink href="/">Privacy Policy</FooterLink>
				<FooterLink href="/">Licensing</FooterLink>
				<FooterLink href="/">Contact</FooterLink>
			</FooterLinkGroup> -->
		</Footer>
	</div>

</div>
