<script>
  import "../app.css"
  import Logo from "./Logo.svelte"
  let scrollY = 0
  $:notOnTop = scrollY !== 0
</script>

<svelte:window bind:scrollY/>

<nav class='z-50 h-20 fixed top-0 w-full px-16 p-4 transition-all flex items-center'>
  <a href='/'>
    <Logo/>
  </a>
  <div class='flex-1'/>
  <ul class='flex bg-white items-center gap-6 shadow-md px-4 h-12 rounded-full'>
    <li class='font-semibold uppercase tracking-wide text-gray-600'>
      Cursos
    </li>
    <li class='font-semibold uppercase tracking-wide text-gray-600'>
      Nosotros
    </li>
    <li class='font-semibold uppercase tracking-wide text-gray-600'>
      Acceso Alumnos
    </li>
  </ul>  
</nav>
<slot></slot>

<style>
</style>