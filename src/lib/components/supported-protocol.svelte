<script lang="ts">
    import Icon from '@iconify/svelte';

    export let iconName: string;
    export let protocolName: string;
    export let description: string = "";
</script>

<li class="flex items-center gap-5 w-full">
    <Icon icon={iconName} font-size=56 />
    <span>
        <b>{protocolName}</b> — {description}
    </span>
</li>