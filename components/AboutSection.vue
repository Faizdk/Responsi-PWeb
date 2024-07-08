<template>
  <link rel='stylesheet' href='https://cdn.jsdelivr.net/npm/bootstrap@4.4.1/dist/css/bootstrap.min.css'>
  
  
  <section class="about">
    <div class="container">
      <div class="content">
        <h1>Hi, I'm Faiz</h1>
        <p>
          I am a student majoring in Informatics at Amikom University Yogyakarta. Currently I have a strong interest in Frontend Web Programming and Database Management.
        </p>
        <button class="btn btn-primary"> Checkout my CV!</button>
      </div>
    </div>
    <div class="image">
        
      </div>
  </section>
  
</template>

<script>
export default {
  name: 'AboutSection'
}
</script>

<style scoped>

* {
  box-sizing: border-box;
}

body {
  background-color: #474e5d;
}
.about {
  position: relative;
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  align-items: center;
  gap: 3rem;
  height: 100vh;
  background-image: url(https://images.unsplash.com/photo-1628882185379-0dd168dfd07a?q=80&w=2008&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D);
}
.about .content {
  margin-left: 5rem;
}

.about .content h1 {
  margin-bottom: 2rem;
  font-size: 3.5rem;
  font-weight: bolder;
  line-height: 3rem;
}

.about .content p {
  font-size: 2rem;
  margin-bottom: 2rem;
  max-width: 800px;
}

.container {
  max-width: 1300px;
  margin: auto;
  padding: 5rem 2rem;
}

.about .image {
  position: relative;
}

.about .image::before {
  position: absolute;
  top: 0;
  left: 50%;
  transform: translateX(-50%);
}

.about .image img {
  max-width: 550px;
  margin: auto;
}

.btn {
  border-radius: 15px;
  margin: 5px;
}
</style>
