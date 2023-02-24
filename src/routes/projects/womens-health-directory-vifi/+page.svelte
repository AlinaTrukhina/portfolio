<script>

    import vifiadmincsv from '$lib/screenCaptures/vifinewslettercsv.mp4'

    // These values are bound to properties of the video
	let paused = true;

	// Used to track time of last mouse down event
	let lastMouseDown;

	// we can't rely on the built-in click event, because it fires
	// after a drag — we have to listen for clicks ourselves
	function handleMousedown(e) {
		lastMouseDown = new Date();
	}

	function handleMouseup(e) {
		if (new Date() - lastMouseDown < 30000) {
			if (paused) e.target.play();
			else e.target.pause();
		}
	}

    const techsUsed = [
    'React',
    'Redux',
    'Sagas',
    'Node.js',
    'Express',
    'PostgreSQL',
    'PassportJS',
    'CSS',
    'Material UI',
    'Nodemailer',
    ]

</script>

<svelte:head>
	<title>Women's Health Directory Web App</title>
	<meta name="description" content="Women's Health Directory Web App" />
</svelte:head>

<section>
    <h1>Women's Health App - ViFi</h1>

    <h2 class=website-link>
        <a href="https://womens-health-app-vifi.herokuapp.com/" target="_blank" rel="noreferrer">
            ViFi website
        </a>
    </h2>

    <h3>Duration: 2 Week Sprint</h3>

    <p>
        The ViFi is a women's health directory app built for our client, Laina Latterner. 
        Laina is an enterpreneur from Minneapolis, MN.
        This app is a collaborative effort from four engineers.
    </p>

    <p>
        The Vifi is our client Laina Latterner's solution to the challenges of women’s health. 
        The goal of the app is to educate and support our targeted users, mainly women, 
        with access to key info about health topics in easy, concise, 
        and timely manner as well as preparation for doctor appointments so 
        women can better advocate for themselves and feel more confident about their healthcare choices. 
        As a mobile webapp, the ViFi is designed to be accessible anytime, anywhere 
        as an educative resource so women can take hold of their healthcare.
    </p>

    <h4>Challenges</h4>
    <p>
        The challenge for this project was about creating a content management system, where Laina 
        could add, edit, or delete the health info for her audience to use. The app is a proof of concept,
        and would likely be adapted for any future uses. For example, the Preventative care section 
        has several categories, with sections such as Guidelines, Diagnostic Tools, FAQs, etc. 
        If other sections are added, they will be able to use the current code for CRUD operations.
    </p>

    <p>
        The ViFi has a newsletter that anyone can sign up for. One feature Laina requested is to be able to 
        download the list of emails to use outside of the app. I used the library 
        <a href="https://www.npmjs.com/package/react-csv">react-csv</a> to accomplish this. The download link is on
        the admin landing page. When clicked, the admin will get a .csv file with the list of emails, which they can export to 
        Microsoft Excel or spreadsheet software of their choice.
    </p>
    <p>
        Another newsletter feature of the Vifi is the ability to edit and send the email right from the app. After trying to 
        implement several text editors and running into roadblock with using React, I've landed on using 
        <a href="http://suneditor.com/sample/index.html">SunEditor</a>. This is a lightweight editor that makes it easy to implement in a React app. 
        It also allows you to edit which features to include in the editor window. The editor included in ViFi allows many options for text editing, 
        as well as addition of images and image edits.
    </p>
    <p>
        Finally, for the last feature of the ViFi newsletter - Laina send the newly written newsletter to her mailing list. I used
        <a href="https://nodemailer.com/about/">Nodemailer</a> to accomplish this task. The implementation involved creating a transported object and 
        specifying username and password for authorization. Since we used a Gmail account, this meant using 2FA for the Gmail account, as well as creating
        an application specific password in the Google account.
    </p>

    <section class="demo">
        <h2>Demo</h2>
        <p>Click on video to play/pause</p>
        <div class="screen-capture">
            <h3>Admin - main page</h3>
            <video class="recording"
            src={vifiadmincsv}
            on:mousedown={handleMousedown}
            on:mouseup={handleMouseup}
            bind:paused>
            <track kind="captions">
        </div>
    </section>

    <h2>Technologies Used</h2>

    <ul>
        {#each techsUsed as tech}
        <li>
            {tech}
        </li>
        {/each}
    </ul>

    <a href="https://github.com/AlinaTrukhina/womens-health-app-ViFi" target="_blank" rel="noreferrer">
        Source Code on GitHub
    </a>
    
</section>

<style>

    p > a {
        color: var(--color-theme-pink);
    }

    p > a:hover {
        background-color: var(--color-theme-purple);
        padding: 3px;
        border-radius: 5px;
    }

    .website-link a {
        color: var(--color-theme-pink);
        font-size: 0.9em;
    }
    
    .website-link a:hover {
        background-color: var(--color-theme-purple);
        padding: 5px;
        border-radius: 5px;
    }
    
    </style>