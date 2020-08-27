<template>
  <div class="mx-auto">
      <v-row justify="center">
    <div class="meteoprog-informer" style="width: 280px" data-params='{"city_ids":"2533","domain":"https://meteoprog.ua/ua","id":"5f47de812bac92e5458b468d","lang":"ua"}'>

      
        <a title="Погода в місті Київ" target="_blank" href="https://meteoprog.ua/ua/weather/Kyiv">
          <img style="margin: 0 auto; display: block" src="https://meteoprog.ua/images/preloader.gif" alt="Loading...">
        </a>
        <a target="_blank" class="constructor__met2wlink" href="https://meteoprog.ua/ua/review/Kyiv/">Погода на 2 тижні</a>
      

      <a class="constructor__metlink" target="_blank" href="https://meteoprog.ua/ua">
        <img style="display: block; margin: 0 auto;" alt="Meteoprog" src="https://meteoprog.ua/images/meteoprog-inf.png">
      </a>
    </div>
      </v-row>
  </div>
</template>

<script>
export default {
  name: "BlockGeo",
};
</script>