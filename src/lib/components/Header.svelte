<script>
  export let mobileMenuOpen = false;
</script>

<nav class="flex items-center justify-between px-6 py-4 max-w-[1400px] mx-auto w-full text-sm font-medium text-gray-600">
  <div class="flex items-center gap-8">
    <a href="/" class="text-black font-bold text-lg tracking-tight flex items-center gap-2">
      <svg class="w-6 h-6" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path
          d="M3.9364 4.8793V10.4948C3.9364 10.662 4.02563 10.8166 4.17048 10.9003L9.0342 13.7087M3.9364 4.8793L9.03472 7.82219M3.9364 4.8793L8.79813 2.07158C8.94299 1.98793 9.12143 1.9879 9.26634 2.0715L14.132 4.8793M9.0342 13.7087L14.132 10.7651M9.0342 13.7087L9.03472 7.82219M9.0342 13.7087V19.3241C9.0342 19.4914 9.12344 19.646 9.26835 19.7296L14.1325 22.5374M9.0342 13.7087L14.1325 16.6516M9.03472 7.82219L14.132 4.8793M14.132 4.8793V10.7651M14.132 10.7651L19.2298 13.7087M14.1325 22.5374V16.6516M14.1325 22.5374L18.9957 19.7296C19.1405 19.646 19.2298 19.4914 19.2298 19.3241V13.7087M14.1325 16.6516L19.2298 13.7087"
          stroke="currentColor"
          stroke-width="1.82353"
          stroke-linejoin="round"
        />
      </svg>
      <span>Replit</span>
    </a>
    
    <div class="hidden lg:flex items-center gap-6">
      <button class="hover:text-black flex items-center gap-1">Features <svg width="10" height="6" viewBox="0 0 10 6" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M1 1L5 5L9 1" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/></svg></button>
      <button class="hover:text-black flex items-center gap-1">Solutions <svg width="10" height="6" viewBox="0 0 10 6" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M1 1L5 5L9 1" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/></svg></button>
      <button class="hover:text-black flex items-center gap-1">Developers <svg width="10" height="6" viewBox="0 0 10 6" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M1 1L5 5L9 1" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/></svg></button>
      <button class="hover:text-black flex items-center gap-1">Resources <svg width="10" height="6" viewBox="0 0 10 6" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M1 1L5 5L9 1" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/></svg></button>
      <a href="/enterprise" class="hover:text-black">Enterprise</a>
      <a href="/pricing" class="hover:text-black">Pricing</a>
    </div>
  </div>

  <div class="flex items-center gap-4">
    <a href="/login" class="hover:text-black hidden sm:block">Log In</a>
    <a href="/signup" class="bg-black text-white px-4 py-2 rounded-full hover:bg-gray-800 transition-colors text-xs font-semibold">Start Building</a>
    <button class="lg:hidden" on:click={() => mobileMenuOpen = !mobileMenuOpen}>
        Menu
    </button>
  </div>
</nav>
