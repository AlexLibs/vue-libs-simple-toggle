<template>
    <label class="vue-libs-simple-toggle">
        <input type="checkbox" v-model="model" :disabled="disabled">
        <span class="slider round"></span>
    </label>
</template>

<script>
    export default {
        data() {
            return {
                model: this.value,
            };
        },
        props: [
            'value',
            'disabled',
        ],
        methods: {
        },
        components: {},
        watch: {
            model: function(){
                this.$emit('input', this.model)
            }
        }
    }
</script>

<style>
    .vue-libs-simple-toggle {
        position: relative;
        display: inline-block;
        width: 60px;
        height: 34px;
    }
    .vue-libs-simple-toggle input {
        display: none;
    }
    .vue-libs-simple-toggle .slider {
        position: absolute;
        cursor: pointer;
        top: 0;
        left: 0;
        right: 0;
        bottom: 0;
        background-color: #ccc;
        -webkit-transition: .4s;
        transition: .4s;
    }
    .vue-libs-simple-toggle .slider:before {
        position: absolute;
        content: "";
        height: 26px;
        width: 26px;
        left: 4px;
        bottom: 4px;
        background-color: white;
        -webkit-transition: .4s;
        transition: .4s;
    }
    .vue-libs-simple-toggle input:checked + .slider {
        background-color: green;
    }
    .vue-libs-simple-toggle input:focus + .slider {
        box-shadow: 0 0 1px green;
    }
    .vue-libs-simple-toggle input:checked + .slider:before {
        -webkit-transform: translateX(26px);
        -ms-transform: translateX(26px);
        transform: translateX(26px);
    }
    .vue-libs-simple-toggle .slider.round {
        border-radius: 34px;
    }
    .vue-libs-simple-toggle .slider.round:before {
        border-radius: 50%;
    }
</style>