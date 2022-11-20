<template>
  <div class="selector-input">
    <label class="placeholder">{{ placeholder }}</label>
    <input type="text" class="input"/>
    <span class="iconfont "></span>
  </div>
</template>

<script>
export default {
    name: 'SelectorInput',
    props:{
        placeholder:{
            type: String,
            default: '请选择'
        }
    }
}

</script>

<style scoped>
.selector-input{
    position: relative;
    width: 100%;
    height: 30px;
}

.input{
    width: 100%;
    height: 100%;
    padding: 0 15px;
    box-sizing: border-box;
    background-color: #fff;
    border: 1px solid #999;
    border-radius: 5px;
    outline: none;
    transition: all .2s linear;
}

.placeholder,.iconfont{
    position: absolute;
}
.placeholder{
    left: 15px;
    top: 5px;
    color: #999;
}

.iconfont{
    right: 15px;
    top: 12px;
    color: #999;
}
</style>
