<script>
  const stats = [
    {
      title: '+35 mil',
      content: 'Estudiantes en toda la academia',
      side: '🎓',
    },
    {
      title: '+4.8',
      content: 'Puntuacion en todos nuestros cursos',
      side: '⭐',
    },
    {
      title: 'Mai Pistiner',
      content: 'Tu instructora <3',
      side: '👩',
    },
  ]
  const blocks = [
    {
      title: 'Curso Oratoria',
      img: 'curso_oratoria.png',
      class: 'col-span-2',
    },
    {
      title: 'Catálogo de cursos',
      img: 'catalogo_cursos.png',
      class: '',
      multiple: true,
    },
    {
      title: 'Acceso alumnos',
      img: 'acceso_alumnos.png',
      class: '',
    },
    {
      title: 'Sobre mí',
      img: 'sobre_mi.png',
      class: '',
    },
    {
      title: 'Mi canal de YouTube',
      img: 'https://th.bing.com/th/id/R.edea5af1b198675b7891f86753202d46?rik=a4FCFz0FNoKVFw&riu=http%3a%2f%2f1000logos.net%2fwp-content%2fuploads%2f2017%2f05%2fyoutube-symbol.jpg&ehk=spn2cCoRnv6FvxVznMwMihkHkgPfVE9izKqDGxuqYsM%3d&risl=&pid=ImgRaw&r=0',
      class: '',
    },
    {
      title: 'Mi podcast',
      img: 'podcast.png',
      class: '',
    },
    {
      title: 'Blog de la academia',
      img: 'blog.png',
      class: 'col-span-2',
    },
  ]

  let scrollY = 0
</script>

<svelte:window bind:scrollY />
<img
  class="opacity-80 -z-10 fixed h-[80vh] top-0 w-full object-cover"
  src="banner.png"
  alt="A banner with Mai Pistiner on it."
/>
<main class="relative h-[80vh]">
  <section
    class="absolute inset-0 grid grid-cols-12 grid-rows-6 overflow-hidden"
  >
    <div
      style={`transform: translateY(${scrollY / 1.8}px)`}
      class="group relative col-start-7 col-end-11 row-start-3 row-end-6"
    >
      <div
        class="absolute group-hover:-translate-y-4 group-hover:-translate-x-4 rounded-xl bg-yellow-300 inset-0 transition-all shadow-md"
      />
      <div
        class="flex group-hover:translate-x-10 group-hover:translate-y-4 transition-all flex-col bg-white rounded-xl h-full translate-x-6 p-8 translate-y-2"
      >
        <p class="pb-4">Descubrí nuestro último curso:</p>
        <p class="text-5xl font-black font-nunito">
          ESTRATEGIAS DE CRECIMIENTO EN REDES SOCIALES 2023
        </p>
        <p class="flex-1" />
        <div class="flex gap-2">
          <a
            href="/cursos"
            class="hover:scale-110 transition-all self-start text-lg font-black hover:bg-gray-900 shadow hover:shadow-lg rounded-xl p-4 bg-black text-white"
          >
            Saber mas
          </a>
          <a
            href="/cursos"
            class="p-4 text-lg font-black text-gray-800 hover:bg-gray-200 hover:shadow-md rounded-xl"
          >
            ver todos los cursos
          </a>
        </div>
        <img
          class="bottom-0 right-0 translate-y-8 translate-x-[30%] absolute h-48"
          src="trending_up.png"
          alt="trending up"
        />
      </div>
    </div>
  </section>
  <section
    class="bg-pink-500 text-white flex gap-8 absolute bottom-0 mx-8 translate-y-[50%] shadow-md p-4 rounded-xl"
  >
    {#each stats as { side, title, content }}
      <div class="p-4 flex gap-2 items-center">
        <p class="text-4xl">
          {side}
        </p>
        <div class="space-y-2 ">
          <p class="text-4xl font-black uppercase tracking-wide font-nunito">
            {title}
          </p>
          <p>
            {content}
          </p>
        </div>
      </div>
    {/each}
  </section>
</main>

<main class="min-h-screen bg-black text-white py-32">
  <section class="max-w-6xl w-full m-auto">
    <p class="text-2xl font-bold text-gray-200">Ofrecemos:</p>
  </section>
  <section class="grid grid-cols-3 gap-4 max-w-6xl w-full m-auto">
    {#each blocks as block}
      <div
        class={'group rounded-xl relative hover:bg-gray-800 p-2 ' + block.class}
      >
        <div
          class="group-hover:shadow-2xl group-hover:scale-105 transition-transform relative h-64"
        >
          {#if block.multiple}
            <div
              class="mx-8 absolute -translate-y-4 group-hover:-translate-y-6 transition-all rounded-xl inset-0 bg-yellow-600"
            />
            <div
              class="mx-4 absolute -translate-y-2 rounded-xl group-hover:-translate-y-3 transition-all inset-0 bg-yellow-500"
            />
          {/if}
          <div class="shadow-inner overflow-hidden rounded-xl absolute inset-0">
            <img
              class="inset-0 object-cover h-full w-full"
              src={block.img}
              alt={block.title}
            />
          </div>
        </div>
        <p
          class="pt-2 text-3xl font-semibold font-nunito group-hover:translate-y-2 transition-transform"
        >
          {block.title}
        </p>
      </div>
    {/each}
  </section>
</main>

<main
  class="min-h-[50vh] px-16 relative grid grid-cols-2 overflow-hidden rounded-t-[2rem] -mt-8 z-10"
>
  <img
    alt="Colorful banner"
    src="waves.svg"
    class="-z-10 absolute left-0 w-full h-full object-cover"
  />
  <section class=" p-8 pr-64 flex items-start flex-col">
    <p class="text-8xl pb-8 font-nunito font-black tracking-wide text-pink-500">
      Nuestra <br /> academia
    </p>
    <p class="text-2xl">
      Desarrollamos cursos de comunicación efectiva, oratoria y estrategias de
      venta para que puedas hablar en público y destacarte en tus habilidades
      interpersonales.
    </p>
  </section>
  <section class="pt-8 flex flex-col items-center">
    <p
      class="text-white text-center font-nunito text-4xl tracking-wide font-bold"
    >
      Más de <strong>35.000</strong> alumnos y<br />
      <strong>40</strong> capacitaciónes a las<br />
      <span class="underline"> mejores empresas!</span>
    </p>
    <img
      class="h-96"
      src="brands.webp"
      alt="The brands that trust Mai Pistiner."
    />
  </section>
</main>

<main class="min-h-[50vh] py-16 bg-white">
  <section class="max-w-6xl mx-auto grid grid-cols-2">
    <div>
      <p class="text-6xl text-pink-500 drop-shadow leading-tight">
        ¡Dejanos tu email<br />
        y recibirás los<br />
        <span class="font-bold tracking-wider">mejores tips</span><br /> por correo!
      </p>
    </div>
    <form
      class="bg-black text-white border-2 p-8 border-gray-600 shadow-lg rounded-xl flex flex-col gap-2"
    >
      <p class="text-4xl font-nunito font-bold tracking-wider mb-4">
        Contactanos!
      </p>
      <label>
        <p>Nombre</p>
        <input
          placeholder="Como te llamas?"
          class="text-black font-bold w-full border-gray-400 shadow-inner border p-2 rounded-md"
          type="text"
        />
      </label>
      <label>
        <p>Mail</p>
        <input
          placeholder="ejemplo@ejemplo.com"
          class="text-black font-bold w-full border-gray-400 shadow-inner border p-2 rounded-md"
          type="mail"
          required
        />
      </label>
      <button
        class="shadow hover:shadow-xl text-xl bg-pink-500 py-2 px-6 self-end mt-8 hover:bg-pink-700 rounded-full text-white font-bold w-fit"
        type="submit">Enviar</button
      >
    </form>
  </section>
</main>
