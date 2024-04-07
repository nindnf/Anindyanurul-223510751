<script setup lang="ts">
defineProps<{
  msg: string
}>()
</script>

<template>
  <div class="greetings">
    <h1 class="black">{{ msg }}</h1>
    <h3>
      Im Anindya Nurul Fadillah
    </h3>
  </div>
  
  <div class="follow-me">
    <ul class="social-media-icons">
      <li>
        <span>Facebook</span>
        <a href="#"><img src="@/assets/Facebook-icon.png" alt="Facebook"></a>
      </li>
      <li>
        <span>Twitter</span>
        <a href="#"><img src="@/assets/twitter-icon.png" alt="Twitter"></a>
      </li>
      <li>
        <span>Instagram</span>
        <a href="https://www.instagram.com/anin_dyarf?igsh=MXRrYW16dDZraDRyYg=="><img src="@/assets/instagram-icon.png" alt="Instagram"></a>
      </li>
    </ul>
  </div>
</template>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 1.5rem;
  position: relative;
  top: -10px;
}

h3 {
  font-size: 1.2rem;
}

.greetings h1,
.greetings h3 {
  text-align: center;
}

@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}

.follow-me {
  position: fixed;
  bottom: 50px;
  left: 10px;
  display: flex;
  align-items: center;
}

.follow-me span {
  margin-right: 10px;
}

.social-media-icons {
  list-style: none;
  padding: 0;
  margin: 0;
}

.social-media-icons li {
  display: inline-block;
  margin-right: 10px;
}

.social-media-icons img {
  width: 30px;
  height: 30px;
}

.social-media-icons span {
  display: block;
  font-size: 12px;
  text-align: center;
}
</style>
