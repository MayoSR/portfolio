<script>
    import BannerContent from "./subcomponents/BannerContent.svelte";
    import SkillWheelDesktop from "./subcomponents/SkillWheelDesktop.svelte";
    import SkillWheelMobile from "./subcomponents/SkillWheelMobile.svelte";
</script>

<div id="intro-banner">
    <BannerContent />
    <SkillWheelDesktop />
    <SkillWheelMobile />
</div>

<style>
    #intro-banner {
        height: 100vh;
        color: white;
        background: #212121;
        display: flex;
    }

    @media (max-width: 780px) {
        #intro-banner {
            height: 100%;
            flex-direction: column;
        }
    }
</style>
