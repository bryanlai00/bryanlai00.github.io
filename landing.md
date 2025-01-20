---
layout: landing
---
<div class="transition-wrapper container">
    <h2 class="intro">hi, i'm bryan.</h2>
    <img class="focus face rounded-circle" src="../img/me.png"/>
     <!-- Create the bubbly, clickable icons for LinkedIn, Resume, Email, and GitHub using Font Awesome -->
    <div class="bubbly-icons">
        <a href="https://www.linkedin.com/in/bryanlais/" target="_blank" class="bubbly-icon">
            <i class="fa-brands fa-linkedin"></i>
        </a>
        <a href="https://docs.google.com/document/d/1fUIPTmvymAzpuX2TjVyDxc5L05BuaFRoxE9Ketp8FQE/edit?usp=sharing" target="_blank" class="bubbly-icon">
            <i class="fa-solid fa-file-pdf"></i>
        </a>
        <a href="mailto:bryanjlais@gmail.com" class="bubbly-icon">
            <i class="fa-solid fa-envelope"></i>
        </a>
        <a href="https://github.com/bryanlais" target="_blank" class="bubbly-icon">
            <i class="fa-brands fa-github"></i>
        </a>
    </div>
</div>


<script>
document.addEventListener("DOMContentLoaded", function () {
    // Preload the jump GIF
    const sitGif = new Image();
    sitGif.src = '../img/sit.gif';

    // Ensure that the background change happens only after the GIF is loaded
    sitGif.onload = function() {
        // Set a timeout to change the background after 5.23 seconds
        setTimeout(function () {
            // Add fade-out effect on body
            document.body.classList.add('loaded');
            // Get the background element
            let background = document.querySelector('.landing');

            // Apply the preloaded background GIF after it's loaded
            background.style.transition = "background-image 1s ease-in-out";
            const newBackground = `url(${sitGif.src})`;
            background.style.backgroundImage = newBackground;

            // No navigation to a new page, only the background change occurs here
        }, 5230);  // Wait for 5.23 seconds before changing the background
    };
});
</script>