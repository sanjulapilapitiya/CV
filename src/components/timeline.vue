<template>
    <div class="container">
        <div class="timeline">
		    <div class="timeline-row">
			    <div class="timeline-time">
				    Currys<small>Sept 2020 - Apr 2023</small>
			    </div>
                <div class="timeline-content">
                    <i class="icon-attachment"></i>
                    <h3>Full-Stack Developer</h3>
                    <p>This is where my commercial experience started, As a junior I was surrounded by talented developers giving me a strong foundation to build on.</p>
                    <p>I've managed to upskill my self quickly and was even trusted to work on the insurance platform as the only dev giving me full autonomy </p>
                    <div class="thumbs">
                        <img class="img-fluid rounded" src="svg/currys-logo.svg" alt="Maxwell Admin">
                    </div>
                    <div>
                        <span class="badge bg-success-subtle border border-success-subtle text-success-emphasis rounded-pill m-1">PHP</span>
                        <span class="badge bg-success-subtle border border-success-subtle text-success-emphasis rounded-pill m-1">MySQL</span>
                        <span class="badge bg-success-subtle border border-success-subtle text-success-emphasis rounded-pill m-1">Twig</span>
                        <span class="badge bg-success-subtle border border-success-subtle text-success-emphasis rounded-pill m-1">Symfony</span>
                        <span class="badge bg-success-subtle border border-success-subtle text-success-emphasis rounded-pill m-1">Behat Test</span>
                        <span class="badge bg-success-subtle border border-success-subtle text-success-emphasis rounded-pill m-1">UnitTest</span>
                    </div>
                </div>
            </div>

            <div class="timeline-row">
                <div class="timeline-time">
                    Evident<small>May 2023 - Present</small>
                </div>
                <div class="timeline-content">
                    <i class="icon-code"></i>
                    <h3>Full-Stack Developer</h3>
                    <p>
                        My work at evident is really when I moved from low-level mid developer to high-mid to senior level. This is due to exposure to more technologies specifically APIs, Vue and being able to get involved in all parts of the delivery cycle, from the discovery stage all the way through to release. 
                    </p>
                    <div class="thumbs">
                        <div class="thumbs">
                        <img class="img-fluid rounded" src="jpg/evident-logo.jpg" alt="Maxwell Admin">
                    </div>
                    </div>
                    <div>
                        <span class="badge bg-success-subtle border border-success-subtle text-success-emphasis rounded-pill m-1">PHP</span>
                        <span class="badge bg-success-subtle border border-success-subtle text-success-emphasis rounded-pill m-1">MySQL</span>
                        <span class="badge bg-success-subtle border border-success-subtle text-success-emphasis rounded-pill m-1">Vue</span>
                        <span class="badge bg-success-subtle border border-success-subtle text-success-emphasis rounded-pill m-1">Symfony</span>
                        <span class="badge bg-success-subtle border border-success-subtle text-success-emphasis rounded-pill m-1">Platform Api</span>
                        <span class="badge bg-success-subtle border border-success-subtle text-success-emphasis rounded-pill m-1">PostgresSQL</span>
                        <span class="badge bg-success-subtle border border-success-subtle text-success-emphasis rounded-pill m-1">Documentation Writing</span>
                        <span class="badge bg-success-subtle border border-success-subtle text-success-emphasis rounded-pill m-1">Nuxt</span>
                    </div>
                </div>
            </div>

            <div class="timeline-row">
                <div class="timeline-content">
                    <p class="m-0">Whats next...</p>
                </div>
            </div>
	    </div>
    </div>
</template>

<script>
    export default {
    name: 'timeline',
    };
</script>

<style scoped>
.timeline {
    position: relative;
    -webkit-border-radius: 4px;
    -moz-border-radius: 4px;
    border-radius: 4px;
    padding: 5rem;
    margin: 0 auto 1rem auto;
    overflow: hidden;
}
.timeline:after {
    content: "";
    position: absolute;
    top: 0;
    left: 50%;
    margin-left: -2px;
    border-right: 2px dashed beige;
    height: 100%;
    display: block;
}

.timeline-row {
    padding-left: 50%;
    position: relative;
    margin-bottom: 30px;
}
.timeline-row .timeline-time {
    position: absolute;
    right: 50%;
    top: 15px;
    text-align: right;
    margin-right: 20px;
    color: white;
    font-size: 1.5rem;
}
.timeline-row .timeline-time small {
    display: block;
    font-size: 0.8rem;
}
.timeline-row .timeline-content {
    position: relative;
    padding: 20px 30px;
    background: beige;
    -webkit-border-radius: 4px;
    -moz-border-radius: 4px;
    border-radius: 4px;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    text-align: center;
}
.timeline-row .timeline-content:after {
    content: "";
    position: absolute;
    top: 20px;
    height: 16px;
    width: 16px;
    background: beige;
}
.timeline-row .timeline-content:before {
    content: "";
    position: absolute;
    top: 20px;
    right: -49px;
    width: 20px;
    height: 20px;
    -webkit-border-radius: 100px;
    -moz-border-radius: 100px;
    border-radius: 100px;
    z-index: 10;
    background: #121212;
    border: 2px dashed beige;
}
.timeline-row .timeline-content h4 {
    margin: 0 0 20px 0;
    overflow: hidden;
    white-space: nowrap;
    text-overflow: ellipsis;
    line-height: 150%;
}
.timeline-row .timeline-content p {
    margin-bottom: 30px;
    line-height: 150%;
}
.timeline-row .timeline-content i {
    font-size: 1.2rem;
    line-height: 100%;
    padding: 15px;
    -webkit-border-radius: 100px;
    -moz-border-radius: 100px;
    border-radius: 100px;
    background: #121212;
    margin-bottom: 10px;
    display: inline-block;
}
.timeline-row .timeline-content .thumbs {
    margin-bottom: 20px;
    display: flex;
}
.timeline-row .timeline-content .thumbs img {
    margin: 5px;
    max-width: 60px;
}
.timeline-row:nth-child(even) .timeline-content {
    margin-left: 40px;
    text-align: left;
}
.timeline-row:nth-child(even) .timeline-content:after {
    left: -8px;
    right: initial;
    border-bottom: 0;
    border-left: 0;
    transform: rotate(-135deg);
}
.timeline-row:nth-child(even) .timeline-content:before {
    left: -52px;
    right: initial;
}
.timeline-row:nth-child(odd) {
    padding-left: 0;
    padding-right: 50%;
}
.timeline-row:nth-child(odd) .timeline-time {
    right: auto;
    left: 50%;
    text-align: left;
    margin-right: 0;
    margin-left: 20px;
}
.timeline-row:nth-child(odd) .timeline-content {
    margin-right: 40px;
}
.timeline-row:nth-child(odd) .timeline-content:after {
    right: -8px;
    border-left: 0;
    border-bottom: 0;
    transform: rotate(45deg);
}

@media (max-width: 992px) {
    .timeline {
        padding: 15px;
    }
    .timeline:after {
        border: 0;
    }
    .timeline .timeline-row:nth-child(odd) {
        padding: 0;
    }
    .timeline .timeline-row:nth-child(odd) .timeline-time {
        position: relative;
        top: 0;
        left: 0;
        margin: 0 0 10px 0;
    }
    .timeline .timeline-row:nth-child(odd) .timeline-content {
        margin: 0;
    }
    .timeline .timeline-row:nth-child(odd) .timeline-content:before {
        display: none;
    }
    .timeline .timeline-row:nth-child(odd) .timeline-content:after {
        display: none;
    }
    .timeline .timeline-row:nth-child(even) {
        padding: 0;
    }
    .timeline .timeline-row:nth-child(even) .timeline-time {
        position: relative;
        top: 0;
        left: 0;
        margin: 0 0 10px 0;
        text-align: left;
    }
    .timeline .timeline-row:nth-child(even) .timeline-content {
        margin: 0;
    }
    .timeline .timeline-row:nth-child(even) .timeline-content:before {
        display: none;
    }
    .timeline .timeline-row:nth-child(even) .timeline-content:after {
        display: none;
    }
}
</style>