<script>
export default {
  name: 'demos-and-on-sale-btns',
  data(){
    return {
      price: '39'
    }
  }
}
</script>

<template>

<div class="box-btns">
  <button class="demos">
    <i width="50" class="fa-solid fa-folder-closed icon"></i>
    <span>Demos</span>
  </button>
  <button class="on-sale">
    <div class="cost">
      <span class="currency">&dollar;</span>
      <span class="price">{{ this.price }}</span>
    </div>
    <span>On Sale</span>
  </button>
</div>

  
</template>



<style lang="scss" scoped>
@use '../../../scss/main.scss' as *;

.box-btns {
  position: absolute;
  right: 30px;
  top: 120px;

  button {
  display: flex;
  flex-direction: column;
  justify-content: center;
  border: 0px;
  background-color: $white;
  width: 70px;
  height: 70px;
  margin: 4px;
  border-radius: 5px;
  font-size: $main-size;
  box-shadow: 0px 10px 15px -3px rgba(0,0,0,0.3);
}

button.on-sale {
  position: relative;
  .price, .currency {
    color: $main-color;
    font-weight: $fw-700;
  }
  .currency {
    position: absolute;
    top: 2px;
    left: 10px;
  }
  .price {
    font-size: 1.6rem;  
  }
}
}


</style>