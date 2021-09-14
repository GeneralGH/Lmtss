<template>
  <div class="search">
    <form action="https://www.baidu.com/s">
      <input
        type="text"
        name="wd"
        class="search__input "
        autocomplete="off"
        autofocus="autofocus"
      />
    </form>
  </div>
</template>

<script>
export default {
  name: "Search",
  setup() {
    
  },
};
</script>

<style lang="scss" scoped>
@import "../../style/reset.scss";

.search {
  display: flex;
  align-items: center;
  justify-content: center;
  margin-top: 50px;
}

.search__input {
  width: 300px;
  height: 50px;
  border-radius: 25px;
  border-style: none;
  box-shadow: 2px 2px 8px;
  text-align: center;
  border: none;
  font-size: 17px;
  background-color: whitesmoke;
  outline: none;
  transition: all 0.2s;
  opacity: 0.7;
}

.search__input:focus {
  width:600px; 
  opacity: 1;
}
</style>