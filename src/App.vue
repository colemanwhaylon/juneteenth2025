<template>
  <div class="container">
    <div class="flag-content">
      <h1>Why are there two flags for Juneteenth?</h1>
      <p class="intro">
        There are two main flags associated with Juneteenth: the official Juneteenth flag and the Pan-African flag...
      </p>

      <div class="flag-row">
        <div class="flag-container">
          <h2>Juneteenth Flag (Red, White, and Blue)</h2>
          <div class="flag-wrapper">
            <FlagComponent title="" image="Juneteenth_Flag.png" alt="Juneteenth Flag" :description="``" />
          </div>
          <div class="flag-info">
            <p><strong>Created by:</strong> Ben Haith in 1997.</p>
            <p><strong>Design:</strong> Starburst symbolizing Texas and new beginnings.</p>
            <p><strong>Colors:</strong> Red, white, and blue representing American citizenship.</p>
          </div>
        </div>

        <div class="flag-container">
          <h2>Pan-African Flag (Red, Black, and Green)</h2>
          <div class="flag-wrapper">
            <FlagComponent title="" image="Juneteenth_Pan_African_Flag.png" alt="Pan-African Flag" :description="``" />
          </div>
          <div class="flag-info">
            <p><strong>Created by:</strong> Marcus Garvey in 1920.</p>
            <p><strong>Colors:</strong> Red (blood), black (people), green (wealth).</p>
            <p><strong>Symbolism:</strong> Black liberation and unity.</p>
          </div>
        </div>
      </div>

      <div class="comparison">
        <h3>Why both flags are used:</h3>
        <p><strong>Juneteenth Flag:</strong> Represents the specific historical emancipation event.</p>
        <p><strong>Pan-African Flag:</strong> Represents broader Black freedom and unification.</p>
      </div>
    </div>
  </div>
</template>

<script>
import FlagComponent from './components/FlagComponent.vue'

export default {
  name: 'App',
  components: {
    FlagComponent
  }
}
</script>

<style>
.container {
  max-width: 1000px;
  margin: 0 auto;
  padding: 20px;
}

.flag-content {
  line-height: 1.6;
}

.intro {
  margin-bottom: 30px;
}

.flag-row {
  display: flex;
  gap: 30px;
  margin-bottom: 40px;
}

.flag-container {
  flex: 1;
}

.flag-wrapper {
  width: 100%;
  height: 300px;
  /* Fixed height for both flags */
  display: flex;
  justify-content: center;
  align-items: center;
  background: #f8f8f8;
  border: 1px solid #eee;
  margin: 15px 0;
  overflow: hidden;
}

.flag-wrapper img {
  width: 100%;
  height: 100%;
  object-fit: contain;
  /* Ensures full flag visibility */
  padding: 10px;
}

.flag-info {
  margin-top: 15px;
}

.comparison {
  background: #f5f5f5;
  padding: 20px;
  border-radius: 5px;
}

@media (max-width: 768px) {
  .flag-row {
    flex-direction: column;
  }

  .flag-wrapper {
    height: 250px;
    /* Slightly smaller on mobile */
  }
}
</style>