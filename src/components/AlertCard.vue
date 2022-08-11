<template>
  <div>
    <p>{{text}}</p>

    <button type="button" @click="fechaItem">
        x
    </button>
  </div>
</template>

<script>
export default {
    name: 'AlertCard',
    props:{
        text: String
    },
    methods:{
        fechaItem(){
            this.$emit('fecha')
        }
    }
}
</script>

<style scoped>
    div{
        width: 100%;
        position: absolute;
        top: 15px;
        left: 0;
        right: 0;
        background: rgb(202, 69, 255);
        color: #fff;
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 20px;
    }
    div button{
        width: 30px;
        border: 0;
        background: transparent;
        color: #fff;
        text-transform: uppercase;
        font-size: 26px;
        cursor: pointer;
    }
</style>