<script lang="ts">
    import { onMount } from "svelte";

    export let strings: string[];

    let whichToShow = 0;
    let visibleSymbols = 0;

    onMount(() => {
        setInterval(() => {
            visibleSymbols = 0;
            whichToShow++;

            if (whichToShow == strings.length) {
                whichToShow = 0;
            }
        }, 3000);

        setInterval(() => {
            if (visibleSymbols == strings[whichToShow].length) {
                return;
            }
            visibleSymbols++;
        }, 50);
    })
</script>

{ #each strings as str, index }
    { #if index == whichToShow }
        <div>
            { #each Array(visibleSymbols) as _, index }
                { str[index] }
            { /each }
        </div>
    { /if }
{/each }