<template>
  <div class="about-page flex flex-col min-h-screen items-center">
    <div class="container mx-auto px-4 py-8 max-w-4xl">
      <div class="bio-section mb-20">
        <div class="flex flex-col lg:flex-row gap-8 items-center lg:items-start">
          <div class="bio-text lg:flex-1">
            <p class="text-md leading-relaxed mb-6 text-justify">
              Leanne Lewis (b.1992) is a Maltese visual artist and art educator. Her research
              and practice mainly revolve around her passion towards the subject of nature and
              the environment within the local context. She explores and interprets topics
              related to landscape, seascapes and environmental concerns through a variety of
              media and techniques including drawing, collage, painting, photography, sculpture
              and installation art.
            </p>

            <p class="text-md leading-relaxed mb-6 text-justify">
              Leanne was part of a number of collective exhibitions held in Malta and her work
              has been also exhibited internationally in London (2020). Leanne teaches visual
              arts at the Malta School of Art in Valletta, and is currently reading for a
              Master of Education in Art at the Institute for Education in Malta. She completed
              her first degree in Fine Arts in 2013, at the Institute of Art and Design, at
              MCAST, and her Master's Degree in Fine Arts in 2016, at the University of Malta.
            </p>
          </div>

          <div class="bio-image lg:flex-shrink-0">
            <img
              src="https://static.wixstatic.com/media/7a2cd6_b8e31d38e1cb45c98f0ec96c24b1c01c~mv2.jpg/v1/crop/x_211,y_0,w_3199,h_4430/fill/w_379,h_525,al_c,q_80,usm_0.66_1.00_0.01,enc_avif,quality_auto/IMG_0246_JPG.jpg"
              alt="Leanne Lewis - Visual Artist" class="rounded-lg shadow-lg max-w-xs w-full h-auto" />
          </div>
        </div>
      </div>

      <div class="exhibitions-section">
        <h2 class="text-2xl font-semibold mb-6">Exhibitions</h2>

        <div class="exhibition-list space-y-4 text-sm">
          <div class="exhibition-year">
            <h3 class="font-semibold text-lg mb-2">2023</h3>
            <ul class="ml-4 space-y-1">
              <li>'MARA #2' collective exhibition - Bureau Iniala, Valletta</li>
            </ul>
          </div>

          <div class="exhibition-year">
            <h3 class="font-semibold text-lg mb-2">2022</h3>
            <ul class="ml-4 space-y-1">
              <li>'The Practice of Practice' collective exhibition - Malta School of Art, Valletta</li>
              <li>'Identity of An Island' collective exhibition - Teatru Astra, Gozo</li>
            </ul>
          </div>

          <div class="exhibition-year">
            <h3 class="font-semibold text-lg mb-2">2020</h3>
            <ul class="ml-4 space-y-1">
              <li>'New Wave' collective exhibition - Boomer gallery, London</li>
            </ul>
          </div>

          <div class="exhibition-year">
            <h3 class="font-semibold text-lg mb-2">2019</h3>
            <ul class="ml-4 space-y-1">
              <li>'Feminae' collective exhibition - Malta Chamber of Commerce, Valletta</li>
              <li>'Perception: Postscripts' collective exhibition - Malta Society of Arts, Palazzo de la Salle, Valletta
              </li>
            </ul>
          </div>

          <div class="exhibition-year">
            <h3 class="font-semibold text-lg mb-2">2018</h3>
            <ul class="ml-4 space-y-1">
              <li>'Levi's Design Contest', collective exhibition - Levi's store, Valletta</li>
              <li>'50 posters for Malta' collective exhibition - Antoine de Paule Hall, San Anton Palace, Attard</li>
            </ul>
          </div>

          <div class="exhibition-year">
            <h3 class="font-semibold text-lg mb-2">2016</h3>
            <ul class="ml-4 space-y-1">
              <li>'MA Fine Arts Final Projects Exhibition' - Splendid, Strait Street, Valletta</li>
            </ul>
          </div>

          <div class="exhibition-year">
            <h3 class="font-semibold text-lg mb-2">2015</h3>
            <ul class="ml-4 space-y-1">
              <li>'Doors: Ten Collages' collective exhibition - Architecture Project AP, Valletta</li>
              <li>'Ziffa' collective exhibition - VeeGeeBee Art Gallery, Valletta</li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.about-page {
  min-height: 100vh;
  padding: 2rem 0;
}

.exhibition-list {
  max-width: 800px;
}

.exhibition-year {
  padding-left: 1.5rem;
  margin-bottom: 1.5rem;
}

.exhibition-year h3 {
  color: #2d3748;
}

.exhibition-year li {
  color: #4a5568;
  line-height: 1.6;
}

.contact-section a {
  font-size: 1.1rem;
  text-decoration: none;
}
</style>