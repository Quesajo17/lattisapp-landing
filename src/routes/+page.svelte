<script>
	import './styles.css';
    import screenshots from '$lib/images/app-screenshots.png';
</script>

<h1>Nothing Great Was Ever Achieved Alone</h1>
<div class="hero">
    <div class="hero-cta">
        <p>Use the power of accountability to follow your long-term goals in the company of friends.</p>
        <div class="app-store-links">
                    <a class="store-link apple-link" href="https://apps.apple.com/us/app/postdrafts/id6455785683?itsct=apps_box_badge&amp;itscg=30200">
                        <img src="https://tools.applemediaservices.com/api/badges/download-on-the-app-store/black/en-us?size=250x83&amp;releaseDate=1604880000" alt="Download on the App Store">
                    </a>
            <a class="store-link" href='https://play.google.com/store/apps/details?id=com.pagefamdesigns.lattis&pcampaignid=pcampaignidMKT-Other-global-all-co-prtnr-py-PartBadge-Mar2515-1'><img alt='Get it on Google Play' src='https://play.google.com/intl/en_us/badges/static/images/badges/en_badge_web_generic.png'/></a>
        </div>
    </div>
    <img src={screenshots} alt="SvelteKit screenshots" />
</div>

<style>
    .hero {
        display: flex;
        align-items: top;
    }

    .hero-cta {
        width: 50%;
    }

    .hero p {
        font-size: 1.5em;
        text-align: left;
    }

    .hero img {
        width: 50%;
        max-width: 600px;
        border-radius: 10px;
        margin: 2em 0;
    }

    .app-store-links {
        display: flex;
        align-items: center;
        margin: 2em 0;
    }

    .store-link {
        display: flex;

    }

    .store-link img {
        width: 200px;
        height: 66px;
        object-fit: contain;
    }

</style>