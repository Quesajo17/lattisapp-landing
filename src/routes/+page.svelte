<script>
	import './styles.css';
    import screenshots from '$lib/images/landing-page-screenshots-narrow.svg';
    import googlebadge from '$lib/images/google-play-badge.svg';
</script>

<h1>Nothing Great Was Ever Achieved Alone</h1>
<div class="hero">
    <div class="hero-cta">
        <p class="hero-text">Use the power of accountability to reach your goals in the company of friends.</p>
        <div class="app-store-links">
                    <a class="store-link apple-link" href="https://apps.apple.com/us/app/lattis-goal-habit-tracker/id6470149396">
                        <img src="https://tools.applemediaservices.com/api/badges/download-on-the-app-store/black/en-us?size=250x83&amp;releaseDate=1604880000" alt="Download on the App Store">
                    </a>
            <a class="store-link-google" href='https://play.google.com/store/apps/details?id=com.pagefamdesigns.lattis'><img alt='Get it on Google Play' src={googlebadge}/></a>
        </div>
    </div>
    <img src={screenshots} alt="SvelteKit screenshots" />
</div>

<style>
    .hero {
        display: inline-block;
        align-items: top;
    }

    .hero-cta {
        width: 100%;
    }

    .hero p {
        font-size: 1.5em;
        text-align: center;
    }

    .hero img {
        width: 100%;
        max-width: 600px;
        border-radius: 10px;
        margin: 2em 0;
    }

    .hero-text {
        font-weight: 700;
    }

    @media (min-width: 750px) {
        

        .hero {
            display: flex;
        }

        .hero img {
            width: 50%;
        }

    }

    @media (min-width: 975px) {
        

        .hero {
            align-items: center;
        }

        .hero-cta {
            align-items: center;
            width: 50%;
        }

        .hero p {
            text-align: left;
        }


    }

    .app-store-links {
        width: 100%;
        display: flex;
        align-items: center;
        justify-content: center;
        margin: 1em 0;
    }

    .store-link {
        display: flex;
        padding: 0 1em;
    }

    .apple-link {
        width: 48%;
    }

    .store-link-google {
        width: 52%;
    }

    .store-link img {
        width: 200px;
        height: 66px;
        object-fit: contain;
    }

    .store-link-google img {
        width: 220px;
        height: 66px;
        object-fit: contain;
        padding-top: 4px;
    }

    @media (max-width: 749px) {
        .store-link img {
        max-width: 200px;
        max-height: 66px;
    }

    .store-link-google img {
        max-width: 220px;
        max-height: 66px;
        object-fit: contain;
        padding-top: 4px;
    }
    }

</style>