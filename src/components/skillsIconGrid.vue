<template>
    <div class="container-fluid px-4 py-5 text-light">
      <div class="row">
        <div class="col-12 col-lg-6" id="icon-grid">
          <h2 class="pb-2 border-bottom">My Skills</h2>
  
          <div class="row row-cols-2 row-cols-md-3 g-4 py-4">
            <div class="col d-flex justify-content-center align-items-center">
              <img class="logo" src="/svg/php-logo.svg" alt="PHP Logo" />
            </div>
            <div class="col d-flex justify-content-center align-items-center">
              <img class="logo" src="/svg/javascript-logo.svg" alt="JavaScript Logo" />
            </div>
            <div class="col d-flex justify-content-center align-items-center">
              <img class="logo" src="/svg/vue-logo.svg" alt="Vue Logo" />
            </div>
            <div class="col d-flex justify-content-center align-items-center">
              <img class="logo" src="/svg/symfony-logo.svg" alt="Symfony Logo" />
            </div>
            <div class="col d-flex justify-content-center align-items-center">
              <img class="logo" src="/svg/apiPlatform-logo.svg" alt="API Platform Logo" />
            </div>
            <div class="col d-flex justify-content-center align-items-center">
              <img class="logo" src="/svg/docker-logo.svg" alt="Docker Logo" />
            </div>
            <div class="col d-flex justify-content-center align-items-center">
              <img class="logo" src="/svg/bootstrap-logo.svg" alt="Bootstrap Logo" />
            </div>
            <div class="col d-flex justify-content-center align-items-center">
              <img class="logo" src="/svg/git-logo.svg" alt="Git Logo" />
            </div>
          </div>
        </div>
  
        <div class="col-12 col-lg-6 d-flex align-items-center justify-content-center">
            <div class="row">
                <div class="col-sm d-flex flex-column align-items-center text-center">
                    <a class="logo" style="max-width: 250px; text-decoration: none;" href="https://www.linkedin.com/public-profile/settings?trk=d_flagship3_profile_self_view_public_profile">
                        <p>
                            Feel free to connect on LinkedIn
                        </p>
                        <img src="/svg/linkedin-logo.svg" alt="LinkedIn Logo" style="max-height: 50px;" />
                    </a>
                </div>
                <div class="col-sm d-flex flex-column align-items-center text-center">
                    <a class="logo" href="/CV.pdf" download="CV.pdf" style="max-width: 250px; text-decoration: none; padding: 5%;">
                        <p>
                            Want to download my CV?
                        </p>
                        <p>
                            CV.pdf  
                            <svg xmlns="http://www.w3.org/2000/svg" width="26" height="26" fill="currentColor" class="bi bi-download" viewBox="0 0 16 16">
                                <path d="M.5 9.9a.5.5 0 0 1 .5.5v2.5a1 1 0 0 0 1 1h12a1 1 0 0 0 1-1v-2.5a.5.5 0 0 1 1 0v2.5a2 2 0 0 1-2 2H2a2 2 0 0 1-2-2v-2.5a.5.5 0 0 1 .5-.5"/>
                                <path d="M7.646 11.854a.5.5 0 0 0 .708 0l3-3a.5.5 0 0 0-.708-.708L8.5 10.293V1.5a.5.5 0 0 0-1 0v8.793L5.354 8.146a.5.5 0 1 0-.708.708z"/>
                            </svg>
                        </p>
                    </a>
                </div>
            </div>
        </div>
  
      </div>
    </div>
  </template>
  
  

<script>
    export default {
    name: 'skillsIconGrid',
    };
</script>

<style scoped>
.logo {
    max-width: 100px;
    max-height: 100px;
    margin-right: 10px;
    filter: grayscale(1);
    transition: filter 0.3s ease;
}
.logo:hover {
  filter: grayscale(0);
}
</style>