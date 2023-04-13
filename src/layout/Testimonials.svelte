<script>
import Testimonial from './testimonials/Testimonial.svelte';

const testimonials = [
  {
    name: '배그핵 제품기능',
    quote: '적ESP/차량ESP/보급/시체박스ESP/에임조준-헤드/에임조준-목/에임조준-몸/에임봇끄기/에임벽뒤 구분/방향키 상 무기ESP/방향키 하 스코프/2~3LV장비/방향키 좌 파츠ESP/방향키 우 의약품ESP/스무스 에임 감도증가/스무스 에임 감도 감소/FOV인식 범위 증가/FOV인식 범위 감소/에임인식 범위 증가/에임인식범위 감소/적 거리ESP/팀원ESP온/오프/아이템ESP아이콘 모드/편의 기능키/ESP폰트크기 증가/ESP폰트크기 감소/플레이어 라인ESP'
  },
  {
    name: '서든핵 제품기능',
    quote: '월핵/에임봇/유도탄/스마트에임/길로틴/방오/방월/즉시리스폰/무반동/에임고정/ESP ( 적위치 표시 )/색변경가능/스켈레톤 ESP 지원/박스 ESP 지원/닉네임 ESP 지원/C4 ESP 지원/수류탄 ESP 지원'
  },
  {
    name: '옵치핵 제품기능',
    quote: '이름 ESP/박스 ESP/궁극기 ESP/테두리 ESP/히트박스 ESP/HUD 사이즈 조절 위치 조정 가능/체력바 ESP (하단,상단 조정가능)/HUD ESP(상대 챔프 및 궁극기)/시각적 ESP색 | 보이는 적 | 보이지 않는 적 | FOV범위에 들어온적/적의 스킬 쿨타임 표시/적이 아나에 의해 치유되지 않으면 체력바 표시/스켈레톤 표시/에이밍 적 라인 표시/조준 한 타겟의 다른 색상'
  }
];
</script>

<section id="testimonials">
  <div class="container">
    <h1>핵마켓 제품소개</h1>
    {#each testimonials as testimonial, i}
      <Testimonial {testimonial} alternate={i % 2 === 1} />
    {:else}
      <em>It appears no one enjoys this web app.</em>
    {/each}
  </div>
</section>

<style>
section {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 1rem 0 2rem;
}

.container {
  max-width: 70rem;
}

h1 {
  margin: 2rem auto;
  margin-bottom: 3rem;
}

@media (min-width: 800px) {
  h1 {
    font-size: 2.4rem;
  }
}

@media (min-width: 1280px) {
  .container {
    width: 75vw;
  }
}
</style>
