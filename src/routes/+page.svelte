<script lang="ts">
    import "$lib/style.css";
    import Swiper from 'swiper';
    import { EffectCards } from 'swiper/modules';
    import 'swiper/css';
    import 'swiper/css/effect-cards';
	import { onMount } from "svelte";

    import adi1 from "$lib/resources/adi_1.png";
    import adi2 from "$lib/resources/adi_2.png";

    let swiperInstance:Swiper;

    onMount(() => {
        swiperInstance = new Swiper(".swiper", {
            effect: "cards",
            modules: [EffectCards],
            grabCursor: true,
            initialSlide: 2,
            speed: 500,
            loop: true,
            mousewheel: {
            invert: false,
            }
        });
        return () => {
        if(swiperInstance) {
            swiperInstance.destroy();
        }
    }
    });

    


</script>

<section>
      <div class="content">
        <div class="info">
            <h1><span class="aditya-hi">Aditya</span> Says Hi!!</h1>
          <p>
            <span class="text-highlight">Full Stack Developer,</span>
            well versed in the following stack:
          </p>
        <ul class="stack">
            <li>ReactJS</li>
            <li>NodeJS</li>
            <li>Svelte</li>
            <li>Sveltekit</li>
            <li>MongoDB</li>
            <li>Redis</li>
            <li>Kafka</li>
            <li>RabbitMQ</li>
            <li>Docker</li>
            <li>Kubernetes</li>
            <li>Python</li>
            <li>Java</li>
            <li>AI</li>
            <li>NLP</li>
            
        </ul>
          <p>Guaranteed development of your web-app in a matter of days.</p>
          <button class="btn">Get in Touch</button>
        </div>
        <div class="swiper">
          <div class="swiper-wrapper">
            <div class="swiper-slide">
              <img
                src={adi1}
                alt="" />
              <div class="overlay">
                <span>Aditya Guru</span>
                <h2>End to end delivery of your web-app in 5 days </h2>
              </div>
            </div>

            <div class="swiper-slide">
              <img
                class="img-position"
                src={adi2}
                alt="" />
              <div class="overlay">
                <span>Aditya Guru</span>
                <h2>7+ Years of industrial Experience</h2>
              </div>
            </div>
             <div class="swiper-slide">
                
              <div class="cards-highlight"> 
                <h1>Served happy customers and helped them grow in business:</h1>
                <br/>
                <ul>
                    <li><a href="https://www.hotelguruestat.com">Hotel Guru Estate</a></li>
                                    <br/>

                    <li><a href="https://www.gymbuddy.com">Gymbuddy</a></li>
                                    <br/>

                    <li><a href="https://www.atithya.co">Atithya Catering</a></li>
                                    <br/>

                    <li><a href="https://www.agarwalsuites.com">Agarwal Suites</a></li>
                </ul>
              </div>
              <div class="overlay">
                <span>High Skilled SEO & Marketting </span>
                <h2>Promoted high growth in 4 weeks</h2>
              </div>
            </div>
          </div>
        </div>
      </div>

      <ul class="circles">
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
      </ul>
    </section>

<style>
    .stack{
       list-style-type: none;
       font-size: 2.2rem;
        background: linear-gradient(180deg, #ffd8d8 0%, #ffc4c4 50%, #ffbdbd 100%);
        -webkit-clip : text;
        -webkit-animation-delay: 2ms;
        -webkit-background-clip: text;
        background-clip: text;
        -webkit-text-fill-color: transparent;
    }
    .stack li{
        display: -webkit-inline-box;
        margin: 0 5px;
        
    }
    .stack li:hover {
        animation: gelatine 0.5s 2;
        background: linear-gradient(180deg, #d8ffd8 0%, #c4ffca 50%, #bdffcf 100%);
        -webkit-clip : text;
        -webkit-animation-delay: 2ms;
        -webkit-background-clip: text;
        background-clip: text;
        -webkit-text-fill-color: transparent;
    }

    

</style>