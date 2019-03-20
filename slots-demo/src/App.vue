<template>
    <div class="container">
        <div class="row">
            <div class="col-xs-12">
                <br>
                <button class="btn btn-primary" @click='changeComponent("appBlue")'>Load Blue Template</button>
                <button class="btn btn-success" @click='changeComponent("appGreen")'>Load Green Template</button>
                <button class="btn btn-danger" @click='changeComponent("appRed")'>Load Red Template</button>
                <hr>
                <component :is="selectedComponent">
                  <p slot='title'>blue</p>
                </component>
            </div>
        </div>
    </div>
</template>

<script>
    import Blue from './components/Blue.vue';
    import Green from './components/Green.vue';
    import Red from './components/Red.vue';

    export default {
        data() {
            return {
                selectedComponent: 'appBlue'
            }
        },
        components: {
            appBlue: Blue,
            appGreen: Green,
            appRed: Red
        },
        methods: {
            changeComponent(c) {
                this.selectedComponent = c
            }
        }
    }
</script>

<style>
</style>
