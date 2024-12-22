<script lang="ts">
    export let src;
    export let alt;

    let toggle: boolean = false;

</script>
<div class="container">
    <button class="card" class:fullscreen={toggle} on:click={()=>toggle = !toggle}>
        <img src="{src}" alt="{alt}"
        class="h-full w-full inset-0 rounded-lg bg-gray-50 {toggle? 'object-contain': 'object-cover'}" />
    </button>
</div>

<style>
 
.container {
  position: relative;
  width: 100%;
  height: 100%;
}

.card {
  position: relative;
  width: 100%;
  height: 100%;
  background-color: #ffffff;
  border: 1px solid #ddd;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.5);
  overflow: hidden;
  cursor: pointer;

  /* Smooth transition for properties */
  transition: all 0.5s ease-in-out;
}

.card.fullscreen {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  border-radius: 0;
  z-index: 9999;
}
</style>