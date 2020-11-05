<template>
    <div>
         <h1>
            {{newComponent}}
        </h1>
        <div>
           <button v-on:click="counter += 1">Add 1</button>
            <p>The button above has been clicked {{ counter }} times.</p>
        </div>
    </div>
</template>

<script>
export default {
    name: "EventHandlers",
    props: {
        newComponent: String
    },
    data : () => {
       return { counter: 0 }
    }
}
</script>

<style>

</style>
