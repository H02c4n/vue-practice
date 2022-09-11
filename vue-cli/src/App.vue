<template>
<app-header/>
<div class="container">
  <h3>This is my first vue-cli</h3>
<p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Quo fuga voluptates adipisci magni nostrum? Omnis illo exercitationem placeat repellat aspernatur quod cupiditate maiores nesciunt, reiciendis, soluta, numquam quisquam nostrum eveniet!</p>
</div>
<counter-item></counter-item>

</template>

<script>
import CounterItem from "@/components/CounterItem";  //Local registering
export default {

  components : {
    CounterItem : CounterItem,
  },
};
</script>
