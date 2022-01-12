<template>
    <ul id="ex1">
        <li>

        </li>
    </ul>
</template>
<script lang="ts">
import { Prop, Component, Vue } from 'vue-property-decorator'

@Component
export default class Test extends Vue {
    @Prop() title!: string

    items!: [{
        
    }]
}
</script>
