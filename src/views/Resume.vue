<template>
  <div class="home">
    <h1>{{ message }}</h1>
    <p></p>
        <!-- Navigation-->
        <nav class="navbar navbar-expand-lg navbar-dark bg-primary fixed-top" id="sideNav">
            <a class="navbar-brand js-scroll-trigger" href="#page-top">
                <span class="d-block d-lg-none">Clarence Taylor</span>
                <span class="d-none d-lg-block"><img class="img-fluid img-profile rounded-circle mx-auto mb-2" src="assets/img/profile.jpg" alt="" /></span>
            </a>
            <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation"><span class="navbar-toggler-icon"></span></button>
            <div class="collapse navbar-collapse" id="navbarSupportedContent">
                <ul class="navbar-nav">
                    <li class="nav-item"><a class="nav-link js-scroll-trigger" href="#about">About</a></li>
                    <li class="nav-item"><a class="nav-link js-scroll-trigger" href="#experience">Experience</a></li>
                    <li class="nav-item"><a class="nav-link js-scroll-trigger" href="#education">Education</a></li>
                    <li class="nav-item"><a class="nav-link js-scroll-trigger" href="#skills">Skills</a></li>
                    <li class="nav-item"><a class="nav-link js-scroll-trigger" href="#interests">Interests</a></li>
                    <li class="nav-item"><a class="nav-link js-scroll-trigger" href="#awards">Awards</a></li>
                </ul>
            </div>
        </nav>
        <!-- Page Content-->
        <div class="container-fluid p-0">
            <!-- About-->
            <section class="resume-section" id="about">
                <div class="resume-section-content">
                    <h1 class="mb-0">
                        {{student.firstName}}
                        <span class="text-primary">{{student.lastName}}</span>
                    </h1>
                    <div class="subheading mb-5">
                        3542 Berry Street · Cheyenne Wells, CO 80810 · (317) 585-8468 ·
                        <a href="mailto:name@email.com">name@email.com</a>
                    </div>
                    <p class="lead mb-5">{{student.shortBio}}</p>
                    <div class="social-icons">
                        <a class="social-icon" href="#"><i class="fab fa-linkedin-in"></i></a>
                        <a class="social-icon" href="#"><i class="fab fa-github"></i></a>
                        <a class="social-icon" href="#"><i class="fab fa-twitter"></i></a>
                        <a class="social-icon" href="#"><i class="fab fa-facebook-f"></i></a>
                    </div>
                </div>
            </section>
            <hr class="m-0" />
            <!-- Experience-->
            <section class="resume-section" id="experience">
                <div class="resume-section-content">
                    <h2 class="mb-5">Experience</h2>
                    <div class="d-flex flex-column flex-md-row justify-content-between mb-5" v-for="experience in student.experience">
                        <div class="flex-grow-1" >
                            <h3 class="mb-0">{{experience.jobTitle}}</h3>
                            <div class="subheading mb-3">{{experience.companyName}}</div>
                            <p>{{experience.details}}</p>
                        </div>
                        <div class="flex-shrink-0"><span class="text-primary">{{experience.startDate}}- {{experience.endDate}}</span></div>
                    </div>
                    <div class="d-flex flex-column flex-md-row justify-content-between mb-5">
                        <div class="flex-grow-1">
                            <h3 class="mb-0">Web Developer</h3>
                            <div class="subheading mb-3">Intelitec Solutions</div>
                            <p>Capitalize on low hanging fruit to identify a ballpark value added activity to beta test. Override the digital divide with additional clickthroughs from DevOps. Nanotechnology immersion along the information highway will close the loop on focusing solely on the bottom line.</p>
                        </div>
                        <div class="flex-shrink-0"><span class="text-primary">December 2011 - March 2013</span></div>
                    </div>
                </div>
            </section>
            <hr class="m-0" />
            <!-- Education-->
            <section class="resume-section" id="education">
                <div class="resume-section-content">
                    <h2 class="mb-5">Education</h2>
                    <div class="d-flex flex-column flex-md-row justify-content-between mb-5">
                        <div class="flex-grow-1" v-for="education in student.education">
                            <h3 class="mb-0">{{ education.universityName }}</h3>
                            <div class="subheading mb-3">{{ education.degree}}</div>
                            <div class="flex-shrink-0"><span class="text-primary">{{ education.startDate }} - {{ education.endDate}} </span></div>
                            <div>{{ education.details}}</div>
                        </div>
                    </div> 
                </div>
            </section>
            <hr class="m-0" />
            <!-- Skills-->
            <section class="resume-section" id="skills">
                <div class="resume-section-content">
                    <h2 class="mb-5">Skills</h2>
                    <ul class="fa-ul mb-0" v-for="skill in student.skills">
                        <li>
                            <span class="fa-li"><i class="fas fa-check"></i></span>
                            {{ skill }} 
                        </li>
                    </ul>
                </div>
            </section>
            <hr class="m-0" />
            <!-- Interests-->
            <section class="resume-section" id="interests">
                <div class="resume-section-content">
                    <h2 class="mb-5">Interests</h2>
                    <p>{{ student.personal }} </p>
                </div>
            </section>
            <hr class="m-0" />

        </div>
  </div>
</template>

<style>
</style>

<script>
export default {
  data: function () {
    return {
      message: "View this resume",
      student: {
        firstName: "Clarence",
        lastName: "Taylor",
        email: "name@email.com",
        phoneNumber: "(317) 585-8468",
        shortBio:
          "I am experienced in leveraging agile frameworks to provide a robust synopsis for high level overviews. Iterative approaches to corporate strategy foster collaborative thinking to further the overall value proposition.",
        linkedInURL: "url here",
        twitterHandle: "twitter handle here",
        personaWebsiteURL: "url here",
        onlineResumeURL: "url",
        githubURL: "url",
        photo: "image",
        personal:
          "Apart from being a web developer, I enjoy most of my time being outdoors. In the winter, I am an avid skier and novice ice climber. During the warmer months here in Colorado, I enjoy mountain biking, free climbing, and kayaking.When forced indoors, I follow a number of sci-fi and fantasy genre movies and television shows, I am an aspiring chef, and I spend a large amount of my free time exploring the latest technology advancements in the front-end web development world.",
        experience: [
          {
            startDate: "March 2013",
            endDate: "Present",
            jobTitle: "senior Web Developer",
            companyName: "Intelitec Solutions",
            details:
              "Capitalize on low hanging fruit to identify a ballpark value added activity to beta test. Override the digital divide with additional clickthroughs from DevOps. Nanotechnology immersion along the information highway will close the loop on focusing solely on the bottom line.",
          },
          {
            startDate: "December 2011",
            endDate: "March 2013",
            jobTitle: "Web Developer",
            companyName: "Intelitec Solutions",
            details:
              "apitalize on low hanging fruit to identify a ballpark value added activity to beta test. Override the digital divide with additional clickthroughs from DevOps. Nanotechnology immersion along the information highway will close the loop on focusing solely on the bottom line.",
          },
          {
            startDate: "July 2010",
            endDate: "December 2011",
            jobTitle: "Junior Web Designer",
            companyName: "Shout! Media Productions",
            details:
              "Podcasting operational change management inside of workflows to establish a framework. Taking seamless key performance indicators offline to maximise the long tail. Keeping your eye on the ball while performing a deep dive on the start-up mentality to derive convergence on cross-platform integration",
          },
        ],
        education: [
          {
            startDate: "August 2006",
            endDate: "May 2010",
            degree: "Bachelor of Science",
            universityName: "University of Colorado, Boulder",
            details: "Computer Science - Web Development Track",
          },
        ],
        skills: [
          "Mobile-First, Responsive Design",
          "Cross Browser Testing & Debugging",
          "Cross Functional Teams",
          "Agile Development & Scrum",
        ],
      },
    };
  },
  created: function () {},
  methods: {
    resumeShow: function () {
      console.log("resume show");
      // resume web request
      axios.get("/api/students/:id").then((response) => {
        console.log(response.data);
        this.student = response.data;
      });
    },
  },
};
</script>




