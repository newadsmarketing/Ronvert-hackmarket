<script>

import Convert from './header/Convert.svelte';
import Compare from './header/Compare.svelte';
import { convertMode, reducedMotion } from '../logic/stores';
import { fade, fly } from 'svelte/transition';
import { bounceOut } from 'svelte/easing';

</script>

<header id="header">
  <div class="container">
    <h2>
      <a href="https://korhack.netlify.com">게임핵마켓</a>
    </h2>
    <div class="hero">
      <div class="hero-text">
        <h1 title="And never will" in:fly={{ x: reducedMotion.gate(-500), duration: 1_500, easing: bounceOut }}>최저가 게임 핵마켓</h1>
        <h2>정지없는 배그핵 서든핵 옵치핵 최저가보장</h2>
      </div>
      <div id="hero-media">
        <img src="./media/box-after.png" alt="Box representing input file" role="presentation">
      </div>
    </div>
    <div class="buttons">
      <button on:click={() => window.location.replace('https://hackmarket.netlify.app/')}>핵마켓 바로가기</button>
    </div>
  </div>
</header>

<style>
header {
  width: 100%;
  padding-top: 1rem;
  background: var(--primary-light);
}

a {
  color: var(--secondary-dark);
  font-weight: 700;
  text-decoration: none;
}

.hero {
  width: 100%;
  display: grid;
  grid-template-columns: 1fr;
  gap: 1rem;
  justify-items: center;
  margin-bottom: 2rem;
}

#hero-media {
  width: 100%;
  max-width: 40rem;
  user-select: none;
  scroll-margin-top: 3rem;
}

.buttons {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 100%;
}

@media (min-width: 640px) {
  h2 {
    align-self: flex-start;
  }

  .buttons {
    flex-direction: row;
    justify-content: space-around;
    gap: 2rem;
    width: auto;
  }
}

@media (min-width: 1280px) {
  .hero {
    width: 100%;
    grid-template-columns: 1fr 1fr;
    grid-auto-rows: auto;
    margin: 2rem;
  }
  .hero > :nth-child(1) {
    grid-column: 1;
  }
  .hero > :nth-child(2) {
    grid-column: 2;
  }

  .hero-text {
    display: flex;
    flex-direction: column;
    justify-content: center;
    text-align: left;
    padding-right: 2rem;
  }

  h1 {
    font-size: 6rem;
    margin-bottom: 0;
  }
  h2 {
    margin-top: 0;
    white-space: nowrap;
  }
}

@media (min-width: 1440px) {
  #hero-media {
    min-width: 25rem;
  }
}

h1,
h2 {
  padding: 1rem 0;
  color: hsl(0, 0%, 10%);
}

h1 {
  font-size: 2.4rem;
  margin: 0;
  padding: 0;
}

h2 {
  line-height: 2.5rem;
  margin: 0;
}
</style>
