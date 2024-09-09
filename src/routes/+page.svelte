<script>
	import './styles.css';
    import screenshots from '$lib/images/landing-page-screenshots-narrow.svg';
    import googlebadge from '$lib/images/google-play-badge.svg';
    import websiteheader from '$lib/images/websiteheader.svg';
    import quickStartImage from '$lib/images/quick-start-guide.png';
    import blueprintImage from '$lib/images/accountability-blueprint-image.png';
    import dailyPageImage from '$lib/images/daily-page-image.svg';
    
    let showPopup = false;

function togglePopup() {
    showPopup = !showPopup;
}

function handleScroll() {
        if (window.scrollY > 100 && !showPopup) { // Adjust the scroll position as needed
            showPopup = true;
            window.removeEventListener('scroll', handleScroll); // Ensure the pop-up appears only once
        }
    }

    // Check if running in the browser
    if (typeof window !== 'undefined') {
        window.addEventListener('scroll', handleScroll);
    }

    function navigateTo(url, newTab = false) {
        if (newTab) {
            window.open(url, '_blank');
        } else {
            window.location.href = url;
        }
        
    }
</script>

<img class="hero-header" src={websiteheader} alt="Lattis Goal & Habit Tracker" />
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
    <img src={screenshots} alt="Lattis app screenshots" />
</div>
<div style="margin: 0 auto;">
    <h2>Resources</h2>
</div>
<div class="landing-page-links">
    <div class="resource">
        <div class="resource-text">
            <h3>Lattis: The App</h3>
            <p>Lattis is a goal tracker designed for group accountability. Set and track goals, habits, and one-off tasks, and create small groups to share progress and send reminders. Lattis is designed to be a companion for your accountability group or partner. Enhance the conversations you're already having with the visual reminder of each person's progress.</p>
        </div>
        <img src={dailyPageImage} alt="Quick Start Guide">
    </div>
    <div class="resource">
        <img src={blueprintImage} style="width:450px; max-width:450px" alt="Accountability Blueprint">
        <div class="resource-text">
            <h3>The Accountability Blueprint</h3>
            <p>There's never been a better time to live a life you're truly proud of. But society doesn't hand us the tools to do that. Having friends who can hold you accountable can be a superpower in doing this. This comprehensive guide comes in two parts: First, the manifesto on why accountability is a sorely-missing part of our culture today, and a guide on how to set up an accountability group of your own to clarify what you want, and start setting and achieving meaningful goals.</p>
            <div class="cta">
                <button on:click={() => navigateTo('/resources/accountability-blueprint.pdf', true)}>Download the Guide</button>
            </div>
        </div>
        
    </div>

    <div class="resource">
        <div class="resource-text">
            <h3>Quick Start Guide</h3>
            <p>Get started with accountability quickly. A simple five-step process to start making progress on your goals now with the help of a friend.</p>
            <div class="resource-cta">
                <button on:click={() => navigateTo('/resources/accountability-quick-start-guide.pdf')}>Download PDF</button>
            </div>
        </div>
        <img src={quickStartImage} alt="Quick Start Guide">
    </div>
</div>

{#if showPopup}
<div class="popup-overlay">
    <div class="popup">
        <button class="close-button" on:click={togglePopup}>&times;</button>
        <h2 class="light">Join the Newsletter</h2>
        <div class="popup-body">
        <p class="light">Get regular ideas on goal-setting, habit-building, and accountability sent to your email.</p>
    </div>
        <iframe src="https://www.blog.lattisapp.com/embed" width="400" height="150" style="background:white;" frameborder="0" scrolling="no"></iframe>
    </div>
</div>
{/if}

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

    .hero-header {
        max-width: 700px;
        margin: 0 auto;
    }

    .landing-page-links {
        margin: 0 0;
        padding: 20px;
        background: transparent;
    }
    .resource {
        display: flex;
        align-items: center;
        margin: 0px 0px 40px;
        padding: 10px;
        background: transparent;
        border-radius: 10px;
    }
    .resource-text {
        flex: 1;
        padding-right: 20px;
        max-width: 50%;
    }
    .resource img {
        max-width: 300px;
        max-height: 400px;
        height: auto;
        margin: 0 auto;
        border-radius: 10px;
    }
    .resource h3 {
        margin-top: 0;
    }
    .resource-cta {
        width: 100%;
        color: #0070f3;
        text-decoration: none;
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
            width: 100%;
        max-width: 200px;
        max-height: 66px;
    }

    .store-link-google img {
        width: 100%;
        max-width: 220px;
        max-height: 66px;
        object-fit: contain;
        padding-top: 4px;
    }
    }

</style>