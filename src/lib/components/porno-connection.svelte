<script lang="ts">
    import Icon from '@iconify/svelte';

    export let iconName: string;
    export let name: string;
    export let url: string;
    export let inverted = false;
</script>

<a href={url} target="_blank">
    <li class={
        "flex items-center justify-center p-3 gap-3 w-full border rounded-xl font-bold transition-all text-xl"
        + (
            inverted
            ? " text-white bg-zinc-900 hover:bg-zinc-600"
            : " border-zinc-500 hover:text-zinc-500 hover:border-zinc-400"
        )
        }>
        <Icon icon={iconName} font-size=24 />
        <span class="flex translate-y-px">
            { name }
        </span>
    </li>
</a>