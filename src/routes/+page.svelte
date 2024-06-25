<script>
    import Slogan from "$lib/components/slogan.svelte";
    import Swiper from 'swiper';
    import { Navigation, Pagination } from 'swiper/modules';
    import 'swiper/css';
    import 'swiper/css';
    import 'swiper/css/pagination';
    import 'swiper/css/navigation';
    import { onMount } from "svelte";
    import Icon from '@iconify/svelte';
    import SupportedProtocol from "$lib/components/supported-protocol.svelte";
    import PornoConnection from "$lib/components/porno-connection.svelte";

    let iconAnimationRender = true;

    onMount(() => {
        const swiper = new Swiper('.swiper', {
            modules: [Navigation, Pagination],
            direction: 'horizontal',
            pagination: {
                el: '.swiper-pagination',
            },
            navigation: {
                nextEl: '.swiper-button-next',
                prevEl: '.swiper-button-prev',
            },
            scrollbar: {
                el: '.swiper-scrollbar',
            },
            edgeSwipeDetection: 'prevent'
        });

        swiper.init();

        setInterval(() => {
            iconAnimationRender = false;
            setTimeout(() => {
                iconAnimationRender = true;
            }, 5);
        }, 4000);
    });

    
</script>
<svelte:head>
    <title>Porno VPN</title>
    <meta name="og:name" content="Porno VPN" />
    <meta name="og:description" content="⚡️ Fast and affordable VPN service, 🐧 A part of @pornofnd project" />
    <meta name="og:image" content="favicon.png" />
</svelte:head>

<h1 class="flex w-full justify-center gap-3 items-center text-5xl font-bold mt-10">
    <img alt="PORNO" src="/favicon.png" width="64" />
    Porno VPN
</h1>

<h2 class="mt-5 text-2xl absolute top-32 left-0 flex justify-center items-center w-full overflow-x-hidden overflow-y-hidden flex-col text-zinc-600">
    <Slogan strings={['Cheap', 'Resistant to blockages', 'Porno']} />
</h2>

<div class="mt-20 flex flex-col gap-10 justify-center py-10 items-center">
    <h1 class="flex w-full justify-center gap-5 text-4xl font-bold items-center px-10">
        <span style="width: 30px; height: 40px;">
            { #if iconAnimationRender }
            <Icon icon="line-md:link" />
            { /if }
        </span>
        Connections
    </h1>
    <ul class="max-w-80 w-full flex flex-col gap-5">
        <PornoConnection iconName="bxs:bot" name="Telegram Bot" inverted url="https://t.me/pornovpnbot" />
        <PornoConnection iconName="mdi:loudspeaker" name="Telegram Channel" url="https://t.me/porno_vpn" />
        <PornoConnection iconName="icomoon-free:bubble" name="Telegram Chat" url="https://t.me/pornovpn_chat" />
        <PornoConnection iconName="mdi:github" name="GitHub" url="https://github.com/pornofnd" />
    </ul>
    <center>
        <a href="#features" class="underline underline-offset-4">Begin a journey</a>
    </center>
</div>

<div id="features" class="mt-3 flex justify-center flex-col items-center gap-10 py-10 px-2 bg-zinc-800 h-screen">
    <h1 class="flex w-full justify-center gap-5 text-4xl font-bold text-white items-center">
        <Icon icon="line-md:star-pulsating-filled-loop" />
        Our features
    </h1>
    <div class="swiper select-none w-full max-w-96 rounded-2xl" style="--swiper-theme-color: white;">
      
        <div class="fill-white text-white swiper-button-prev -translate-x-2 scale-50"></div>
        <div class="fill-white text-white swiper-button-next translate-x-2 scale-50"></div>
        
        <div class="swiper-wrapper">
            <div class="swiper-slide">
                <img class="rounded-2xl w-screen" alt="slide" src="/slides/1.png" />
            </div>
            <div class="swiper-slide">
                <img class="rounded-2xl" alt="slide" src="/slides/2.png" />
            </div>
            <div class="swiper-slide">
                <img class="rounded-2xl" alt="slide" src="/slides/3.png" />
            </div>
            <div class="swiper-slide">
                <img class="rounded-2xl" alt="slide" src="/slides/4.png" />
            </div>
            <div class="swiper-slide">
                <img class="rounded-2xl" alt="slide" src="/slides/5.png" />
            </div>
            <div class="swiper-slide">
                <img class="rounded-2xl" alt="slide" src="/slides/6.png" />
            </div>
        </div>
        <div class="swiper-pagination"></div>
      
        <div class="swiper-scrollbar"></div>
    </div>
</div>

<div class="pt-10 flex flex-col gap-10 justify-center py-10 items-center bg-zinc-800 text-white">
    <h1 class="flex w-full justify-center gap-5 text-4xl font-bold items-center px-10">
        <Icon icon="line-md:cog-filled-loop" />
        Supported Protocols
    </h1>
    <ul class="max-w-80 w-full flex flex-col gap-5">
        <SupportedProtocol iconName="arcticons:wireguard" protocolName="WireGuard" description="For high connection speed" />
        <SupportedProtocol iconName="arcticons:v2rayng" protocolName="VLESS and VMess" description="For bypassing any restrictions" />
    </ul>
</div>

<div class="mt-10 flex flex-col gap-10 justify-center py-10 items-center">
    <h1 class="flex w-full justify-center gap-5 text-4xl font-bold items-center px-10">
        <span style="width: 60px; height: 60px;">
            { #if iconAnimationRender }
            <Icon icon="line-md:gauge-full" />
            { /if }
        </span>
        Key System
    </h1>
    <ul class="max-w-80 w-full flex flex-col gap-5">
        <li class="flex items-center gap-5">
            <Icon icon="mdi:gift" font-size=32 />
            <span>
                Ability to gift subscriptions
            </span>
        </li>
        <li class="flex items-center gap-5">
            <Icon icon="fluent-mdl2:distribute-down" font-size=32 />
            <span>
                Ability to distribute subscriptions
            </span>
        </li>
    </ul>
</div>

<div class="pt-10 flex flex-col gap-10 justify-center py-10 items-center">
    <h1 class="flex w-full justify-center gap-5 text-4xl font-bold items-center px-10">
        <span style="width: 60px; height: 60px;">
            { #if iconAnimationRender }
            <Icon icon="line-md:switch-filled" font-size=52 />
            { /if }
        </span>
        Slot system
    </h1>
    <ul class="max-w-80 w-full flex flex-col gap-5">
        <li class="flex items-center gap-5">
            <Icon icon="gala:multi" font-size=56 />
            <span>
                Purchase additional slots for your VPN configurations, for using them on different devices simultaneously
            </span>
        </li>
    </ul>
</div>

<div class="pt-10 flex flex-col gap-10 justify-center py-10 items-center">
    <h1 class="flex w-full justify-center gap-5 text-4xl font-bold items-center px-10">
        <Icon icon="line-md:uploading-loop" />
        Rotation
    </h1>
    <ul class="max-w-80 w-full flex flex-col gap-5">
        <li class="flex items-center gap-5">
            <Icon icon="material-symbols:globe" font-size=56 />
            <span>
                Change regions without altering your VPN configuration // Works on all protocols
            </span>
        </li>
    </ul>
</div>

<div class="pt-10 flex flex-col gap-10 justify-center py-10 items-center bg-zinc-800 text-white">
    <Icon icon="simple-icons:ton" font-size=40 width=40 />
    <h1 class="flex w-full justify-center gap-5 text-4xl font-bold items-center px-10">
        Integration with  TON Cryptocurrency
    </h1>
    <ul class="max-w-80 w-full flex flex-col gap-5">
        <li class="flex items-center gap-5">
            <Icon icon="material-symbols:lock" font-size=29 />
            <span>
                Pay with crypto
            </span>
        </li>
        <li class="flex items-center gap-5">
            <Icon icon="arcticons:tonkeeper" font-size=64 />
            <span>
                Connect your favorite TON Wallet // We will use it to back up your profile
            </span>
        </li>
        <li class="flex items-center gap-5">
            <Icon icon="mdi:anonymous" font-size=32 />
            <span>
                Remain anonymous
            </span>
        </li>
    </ul>
</div>

<div class="pt-10 flex flex-col gap-10 justify-center py-10 items-center">
    <h1 class="flex w-full justify-center gap-5 text-4xl font-bold items-center px-10">
        <span style="width: 60px; height: 60px;">
            { #if iconAnimationRender }
            <Icon icon="line-md:map-marker-multiple-alt-filled" font-size=34 style="width: 60px; height: 60px;" />
            { /if }
        </span>
        Supported countries
    </h1>
    <ul class="max-w-80 w-full flex flex-col gap-5">
        <li class="flex items-center gap-3">
            <Icon icon="twemoji:flag-brazil" font-size=36 style="width: 60px;" />
            <b>Brazil</b>
        </li>
        <li class="flex items-center gap-3">
            <Icon icon="twemoji:flag-france" font-size=36 style="width: 60px;" />
            <b>France</b>
        </li>
        <li class="flex items-center gap-3">
            <Icon icon="twemoji:flag-germany" font-size=36 style="width: 60px;" />
            <b>Germany</b>
        </li>
    </ul>
</div>

<div class="pt-10 flex flex-col gap-10 justify-center py-10 items-center">
    <h1 class="flex w-full justify-center gap-3 text-4xl font-bold items-center px-10">
        <Icon icon="line-md:account-alert-loop" font-size=42 style="width: 60px;" />
        <span class="w-96">And remember...</span>
    </h1>
    <ul class="max-w-80 w-full flex flex-col gap-5">
        It's not meant to be confused with pornographic content!

        <br><br>

        <img alt="PORNO" class="rounded-xl w-full" src="porno.png" />
    </ul>
</div>