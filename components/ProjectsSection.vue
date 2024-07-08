<template>
  <link rel='stylesheet' href='https://cdn.jsdelivr.net/npm/bootstrap@4.4.1/dist/css/bootstrap.min.css'>
  <section class="projects">
    <!-- Tambahkan daftar proyek di sini -->
    <h1>My Recent Projects</h1>
    <ul>
        <li style="--accent-color:#41516C">
            <div class="date">2024</div>
            <div class="title">Suki Sushi ~ Website</div>
            <div class="descr">Project yang mengembangkan sebuah website inovatif untuk Restoran Sushi yang memiliki desain yang ringan. Fokus kami adalah menciptakan sebuah platform yang tidak hanya mempersembahkan menu sushi dengan jelas dan menarik, tetapi juga memberikan pengalaman pengguna yang lancar dan efisien.</div>
        </li>
        <li style="--accent-color:#FBCA3E">
            <div class="date">2023</div>
            <div class="title">HeartSync ~ Smartwatch Application</div>
            <div class="descr">Sebuah Aplikasi khusus smartwatch yang ditujukan untuk membantu mencegah terjadinya kasus serangan jantung bagi orang orang yang sudah berumur, ataupun bagi kalangan lainnya yang memerlukan.</div>
        </li>
        <li style="--accent-color:#E24A68">
            <div class="date">2022</div>
            <div class="title">Coca Cola ~ Commercial</div>
            <div class="descr">Sebuah Iklan Singkat untuk produk Coca cola yang dibuat menggunakan Adobe Premiere Pro.</div>
        </li>
        <li style="--accent-color:#1B5F8C">
            <div class="date">2022</div>
            <div class="title">Tentang Rumahku ~ Music Video</div>
            <div class="descr">Music Video lagu Tentang Rumahku karya Dialog Dini Hari. Software yang Digunakan adalah Adobe Premiere Pro</div>
        </li>
        <li style="--accent-color:#4CADAD">
            <div class="date">2022</div>
            <div class="title">Stilli Da Donna ~ Magazine</div>
            <div class="descr">Majalah Fashion yang berisi seputar Dunia Fashion wanita menggunakan Software Adobe Photoshop dan Adobe InDesign..</div>
        </li>
    </ul>
  </section>
</template>

<script>
export default {
  name: 'ProjectsSection'
}
</script>

<style scoped>
.projects {
  padding: 50px 0;
  background-image: url(https://images.unsplash.com/photo-1628882185379-0dd168dfd07a?q=80&w=2008&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D);
}

.projects h1 {
  margin-top: 100px;
  margin-bottom: 50px;
}
*,
*::before,
*::after {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  --color: rgba(30, 30, 30);
  --bgColor: rgba(245, 245, 245);
  min-height: 100vh;
  display: grid;
  align-content: center;
  gap: 2rem;
  padding: 2rem;
  color: var(--color);
  background: var(--bgColor);
}

h1 {
  text-align: center;
  color: black;
}

ul {
  --col-gap: 2rem;
  --row-gap: 2rem;
  --line-w: 0.25rem;
  display: grid;
  grid-template-columns: var(--line-w) 1fr;
  grid-auto-columns: max-content;
  column-gap: var(--col-gap);
  list-style: none;
  width: min(60rem, 90%);
  margin-inline: auto;
}

/* line */
ul::before {
  content: "";
  grid-column: 1;
  grid-row: 1 / span 20;
  background: rgb(240, 240, 240);
  border-radius: calc(var(--line-w) / 2);
}

/* columns*/

/* row gaps */
ul li:not(:last-child) {
  margin-bottom: var(--row-gap);
}

/* card */
ul li {
  grid-column: 2;
  --inlineP: 1.5rem;
  margin-inline: var(--inlineP);
  grid-row: span 2;
  display: grid;
  grid-template-rows: min-content min-content min-content;
}

/* date */
ul li .date {
  --dateH: 3rem;
  height: var(--dateH);
  margin-inline: calc(var(--inlineP) * -1);

  text-align: center;
  background-color: var(--accent-color);

  color: white;
  font-size: 1.25rem;
  font-weight: 700;

  display: grid;
  place-content: center;
  position: relative;

  border-radius: calc(var(--dateH) / 2) 0 0 calc(var(--dateH) / 2);
}

/* date flap */
ul li .date::before {
  content: "";
  width: var(--inlineP);
  aspect-ratio: 1;
  background: var(--accent-color);
  background-image: linear-gradient(rgba(0, 0, 0, 0.2) 100%, transparent);
  position: absolute;
  top: 100%;

  clip-path: polygon(0 0, 100% 0, 0 100%);
  right: 0;
}

/* circle */
ul li .date::after {
  content: "";
  position: absolute;
  width: 2rem;
  aspect-ratio: 1;
  background: var(--bgColor);
  border: 0.3rem solid var(--accent-color);
  border-radius: 50%;
  top: 50%;

  transform: translate(50%, -50%);
  right: calc(100% + var(--col-gap) + var(--line-w) / 2);
}

/* title descr */
ul li .title,
ul li .descr {
  background: var(--bgColor);
  position: relative;
  padding-inline: 1.5rem;
}
ul li .title {
  overflow: hidden;
  padding-block-start: 1.5rem;
  padding-block-end: 1rem;
  font-weight: 700;
  font-size: 20px;
}
ul li .descr {
  padding-block-end: 1.5rem;
  font-weight: 400;
  font-size: 18px;
}

/* shadows */
ul li .title::before,
ul li .descr::before {
  content: "";
  position: absolute;
  width: 90%;
  height: 0.5rem;
  background: rgba(0, 0, 0, 0.5);
  left: 50%;
  border-radius: 50%;
  filter: blur(4px);
  transform: translate(-50%, 50%);
}
ul li .title::before {
  bottom: calc(100% + 0.125rem);
}

ul li .descr::before {
  z-index: -1;
  bottom: 0.25rem;
}

@media (min-width: 40rem) {
  ul {
    grid-template-columns: 1fr var(--line-w) 1fr;
  }
  ul::before {
    grid-column: 2;
  }
  ul li:nth-child(odd) {
    grid-column: 1;
  }
  ul li:nth-child(even) {
    grid-column: 3;
  }

  /* start second card */
  ul li:nth-child(2) {
    grid-row: 2/4;
  }

  ul li:nth-child(odd) .date::before {
    clip-path: polygon(0 0, 100% 0, 100% 100%);
    left: 0;
  }

  ul li:nth-child(odd) .date::after {
    transform: translate(-50%, -50%);
    left: calc(100% + var(--col-gap) + var(--line-w) / 2);
  }
  ul li:nth-child(odd) .date {
    border-radius: 0 calc(var(--dateH) / 2) calc(var(--dateH) / 2) 0;
  }
}

</style>
