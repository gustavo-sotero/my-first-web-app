<template>
  <header class="header" ref="headershadow" v-bind:class="{ scroll: toggle_shadow_header }">
    <nav class="header-navbar container" v-bind:class="{ show: toggle_menu }">
      <a href="#" class="header-navbar-logo">
        Origin - <span>Notz</span>.
      </a>
      <div class="header-navbar-menu">
        <ul class="grid">
          <li><a class="title" href="#home" @click="removeMenu('home')" v-bind:class="{ active : is_active == 'home' }">Home</a></li>
          <li><a class="title" href="#tech" @click="removeMenu('tech')" v-bind:class="{ active : is_active == 'tech' }">Tech Usadas</a></li>
          <li><a class="title" href="#carrousels" @click="removeMenu('carrousels')" v-bind:class="{ active : is_active == 'carrousels' }">Carrossel</a></li>
        </ul>
      </div>
      <div class="toggle icon icon-menu" @click="toggleMenu"></div>
      <div class="toggle icon icon-close" @click="toggleMenu"></div>
    </nav>
  </header>
  <main>

    <section class="section" id="home">
      <div class="container grid">
        <div class="section-image">
          <img src="./assets/img/developer.png" alt="Notebook Ilustrativo." />
        </div>
        <div class="section-content">
          <h2 class="title">Este é meu primeiro projeto Front-End Usando Vue.</h2>
          <p>
            Olá meu nome é Gustavo sou desenvolvedor web e essa é minha primeira aplicação web.<br />Já Desenvolvo à algum tempo porem nunca curti muito o lado do front-end, mas resolvi isso e essa é a minha primeira aplicação web front-end.
          </p>
        </div>
      </div>
    </section>

    <div class="divider"></div>

    <section class="section" id="tech">
      <div class="container grid">
        <header>
          <h2 class="title">Algumas Informações Sobre a Aplicação.</h2>
          <p>
            Este aplicação foi totalmente desenvolvida em VueJS. Desenvolvi este projeto para melhorar minhas habilidades com HTML e CSS.
          </p>
        </header>
        <div class="cards grid">
          <div class="card">
            <i class="icon icon-vuejs-brands"></i>
            <h2 class="title">VueJS</h2>
            <p>Utilizei VueJS para aprender mais sobre o framework e criar mais 'intimidade' com o framework.<br /><br />Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quis quae aperiam minus enim natus asperiores tempore reprehenderit hic atque ad? Dolor modi aperiam perferendis natus quaerat facere expedita reprehenderit omnis.</p>
          </div>
          <div class="card">
            <i class="icon icon-logo-html5"></i>
            <h2 class="title">HTML</h2>
            <p>Este projeto me ajudou muito a aprender mais sobre HTML e também aprendi bastante sobre SEO. agora me sinto mais intimo do HTML.<br /><br />Lorem ipsum dolor sit, amet consectetur adipisicing elit. Minus qui voluptate culpa odit vel dolore aliquid atque ullam natus fuga. Laudantium labore dolorum sint! Officiis nobis quae consequuntur obcaecati nostrum.</p>
          </div>
          <div class="card">
            <i class="icon icon-logo-css3"></i>
            <h2 class="title">CSS</h2>
            <p>Também desenvolvi muito minha habilidades de CSS agora entendo como estilizar uma pagina e como torna uma aplicação responsiva.<br /><br />Lorem ipsum dolor sit amet consectetur adipisicing elit. Officia ad laborum illum iure, fugit quis soluta? Voluptate qui, iure eum totam impedit quis officiis quos tenetur veritatis cum enim aperiam?</p>
          </div>
        </div>
      </div>
    </section>

    <div class="divider"></div>

    <section class="section" id="carrousels">
      <div class="container">
        <div class="section-content">
          <h2 class="title">Seção De Carrossel.</h2>
          <p class="subtitle">Fiz esta seção para entender mais sobre como importar uma lib para vue.</p>
          <swiper
            :modules="modules"
            :slides-per-view="slides_per_views"
            :pagination="{ clickable: true }"
          >
          <swiper-slide>
            <div class="carrousel">
            <blockquote>
              <p>
                <span>&ldquo;</span>
                Lorem ipsum dolor sit amet consectetur adipisicing elit.
                Rerum blanditiis saepe nam excepturi explicabo ipsa error
                ipsam neque
              </p>
              <cite>
                <img src="https://picsum.photos/300/300?random=1" alt="Foto de Wanessa Souza" />
                Romario Souza
              </cite>
            </blockquote>
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="carrousel">
              <blockquote>
                <p>
                  <span>&ldquo;</span>
                  Lorem ipsum dolor sit amet consectetur adipisicing elit.
                  Rerum blanditiis saepe nam excepturi explicabo ipsa error
                  ipsam neque
                </p>
                <cite>
                  <img src="https://picsum.photos/300/300?random=2" alt="Foto de Wanessa Souza" />
                  Roberto André
                </cite>
              </blockquote>
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="carrousel">
              <blockquote>
                <p>
                  <span>&ldquo;</span>
                  Lorem ipsum dolor sit amet consectetur adipisicing elit.
                  Rerum blanditiis saepe nam excepturi explicabo ipsa error
                  ipsam neque
                </p>
                <cite>
                  <img src="https://picsum.photos/300/300?random=3" alt="Foto de Wanessa Souza" />
                  João Pedro
                </cite>
              </blockquote>
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="carrousel">
              <blockquote>
                <p>
                  <span>&ldquo;</span>
                  Lorem ipsum dolor sit amet consectetur adipisicing elit.
                  Rerum blanditiis saepe nam excepturi explicabo ipsa error
                  ipsam neque
                </p>
                <cite>
                  <img src="https://picsum.photos/300/300?random=4" alt="Foto de Wanessa Souza" />
                  Vitor Almeida
                </cite>
              </blockquote>
            </div>
          </swiper-slide>
          </swiper>
        </div>
      </div>
    </section>
  </main>

  <footer>
    <section class="section" id="footer">
      <div class="container grid">
        <div class="section-content">
          <h2 class="title">Meus Contatos.</h2>
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Culpa, officiis. Alias numquam laborum dolor eius quaerat enim asperiores facilis excepturi sint? Voluptatem, mollitia libero. Ipsum hic incidunt aliquam fuga id?
          </p>
        </div>
        <div class="links">
          <ul class="grid">
            <li><i class="icon icon-github-brands"></i> <a class="link" href="https://github.com/gustavosantos13" target="_blank">gustavosantos13</a> </li>
            <li><i class="icon icon-telegram-plane"></i> <a class="link" href="https://t.me/GustaOfficial" target="_blank">@GustaOfficial</a> </li>
            <li><i class="icon icon-discord-brands"></i> <span class="link">Gustavo -v#6200</span> </li>
          </ul>
        </div>
      </div>
    </section>
  </footer>
</template>

<script>

import { Navigation, Pagination, Scrollbar, A11y } from 'swiper';

// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from 'swiper/vue';

// Import Swiper styles
import 'swiper/css';
import 'swiper/css/navigation';
import 'swiper/css/pagination';
import 'swiper/css/scrollbar';


export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  name: 'App',
  created () {
    window.addEventListener('scroll', this.toggleShadowHeader);
    window.addEventListener('resize', this.slidePerView);
  },
  data() {
    return {
      toggle_menu: false,
      slides_per_views: 1,
      is_active: '',
      toggle_shadow_header: false
    }
  },
  methods: {
    toggleMenu() {
      return this.toggle_menu = !this.toggle_menu;
    },
    removeMenu(tab_active) {
      this.is_active = tab_active;
      return this.toggle_menu = false;
    },
    toggleShadowHeader () {
      if (window.scrollY >= this.$refs.headershadow.clientHeight) {
        this.toggle_shadow_header = true;
      } else {
        this.toggle_shadow_header = false;
      }
    },
    slidePerView () {
      if (this.$refs.headershadow.clientWidth >= 1023) {
        this.slides_per_views = 2;
      } else {
        this.slides_per_views = 1;
      }
    }
  },
  beforeUnmount() {
    window.removeEventListener('scroll', this.toggleShadowHeader);
  },
  mounted(){
    this.slidePerView();
  },
  setup() {
    return {
      modules: [Navigation, Pagination, Scrollbar, A11y],
    }
  }

};
</script>

<style scoped>
@import '@/assets/icons/css/icons.css';
@import '@/assets/css/main.css';
</style>

