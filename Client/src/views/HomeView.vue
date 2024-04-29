<template>
  <div class="max-h-screen">
    <NavbarHome
      class="animate__animated animate__fadeInDown animate__delay-1s" />

    <div class="flex flex-col lg:flex-row items-center justify-center py-10">
      <!-- Bagian teks di kiri -->
      <div class="lg:w-1/2 xl:w-1/2 text-center lg:text-left">
        <!-- Transisi dan teks "Transcend" -->
        <transition name="custom" class="animate__animated animate__fadeInLeft">
          <h1
            class="text-2xl mx-5 mb-3 mt-5 sm:text-3xl lg:mx-20 lg:text-3xl xl:text-3xl tracking-widest font-quicksand">
            Transcend the boundaries of elegance with
          </h1>
        </transition>

        <!-- Transisi dan teks "GLAMOUR GATEWAY" -->
        <transition
          name="custom"
          class="animate__animated animate__fadeInUp animate__delay-1s">
          <h2
            class="mx-20 mt-2 mb-3 font-semibold text-3xl tracking-widest sm:text-3xl md:text-4xl lg:mx-20 lg:text-4xl xl:text-4xl">
            GLAMOUR GATEWAY
          </h2>
        </transition>

        <!-- Teks deskriptif -->
        <div class="animate__animated animate__fadeInUp animate__delay-1s">
          <p
            class="mx-5 mt-2 mb-10 text-lg lg:text-lg lg:mx-20 xl:text-lg tracking-normal font-quicksand">
            Experience the magic of a radiant and youthful complexion
          </p>

          <!-- Tombol Shop Now -->
          <a
            href="#learn-more"
            class="mt-4 ml-5 mr-2 lg:ml-20 bg-slate-800 text-white py-2 px-4 rounded-sm hover:bg-slate-900 transition duration-300">
            Learn More
          </a>
          <a
            href="#learn-more"
            class="mt-4 mr-5 lg:mr-20 bg-slate-800 text-white py-2 px-4 rounded-sm hover:bg-slate-900 transition duration-300">
            Shop Now
          </a>
        </div>
      </div>

      <!-- Bagian gambar di kanan -->

      <transition name="custom" class="animate__animated animate__slideInDown">
        <div class="mt-7 lg:w-[55%] h-full">
          <img src="../assets/monochrome-heroImage.png" alt="Hero Image" />
        </div>
      </transition>
    </div>

    <!-- Promotional Offers Section -->
    <div class="mt-20 mx-10 sm:mx-10 md:mx-10 lg:mx-20 py-12">
      <div class="container mx-auto px-4">
        <h2 class="text-3xl tracking-widest font-switzer text-right mb-8">
          * Promotional Offers
        </h2>
        <div class="grid grid-cols-1 sm:grid-cols-2 gap-8">
          <!-- Promotion 1 -->
          <div class="p-6 rounded-lg shadow-md bg-slate-900 text-white">
            <h3 class="text-xl font-semibold mb-4 text-white">
              20% Off Weekend Sale
            </h3>
            <p class="text-white">
              Get 20% off on all products this weekend! Use code: WEEKEND20.
              Hurry, offer ends soon!
            </p>
          </div>
          <!-- Promotion 2 -->
          <div class="p-6 rounded-lg shadow-md bg-slate-900 text-white">
            <h3 class="text-xl font-semibold mb-4 text-white">
              Newsletter Signup Discount
            </h3>
            <p class="text-white">
              Sign up for our newsletter and receive a $10 discount on your
              first purchase!
            </p>
          </div>
        </div>
      </div>
    </div>

    <!-- Featured Products Section -->
    <div class="mt-20 h-[1000px]">
      <!-- Title for the featured products section -->
      <transition
        name="custom"
        class="animate__animated animate__fadeInUp animate__delay-1s">
        <p class="ml-20 mt-20 text-3xl tracking-widest font-switzer">
          * Featured Products
        </p>
      </transition>

      <div class="flex mx-20">
        <!-- First Carousel -->
        <Carousel
          :itemsToShow="3.7"
          :wrapAround="true"
          :transition="1000"
          :autoplay="3000"
          class="overflow-hidden">
          <!-- Products for the first carousel -->
          <Slide
            v-for="(product, index) in products"
            :key="index"
            class="-mx-2">
            <div class="font-quicksand mt-10 mx-5 text-left w-[300px]">
              <img
                :src="product.image"
                class="w-full h-64 object-cover mb-4"
                alt="Product Image" />
              <div class="px-4">
                <div
                  class="font-bold text-base md:text-xs lg:text-lg mb-2 text-gray-900 overflow-hidden">
                  {{ product.name }}
                  <p
                    class="text-gray-700 text-sm md:text-xs lg:text-md h-4 font-medium">
                    Pruduct Category - From Korea
                  </p>
                </div>

                <p
                  class="text-gray-700 text-sm md:text-xs lg:text-md h-4 mb-4 overflow-y-auto">
                  Description
                </p>
              </div>
              <div
                class="px-2 py-2 sm:px-2 sm:py-2 md:px-2 md:py-2 lg:px-4 lg:py-4 flex justify-between items-center bg-slate-800">
                <p
                  class="text-white text-xs sm:text-xs md:text-xs lg:text-md xl:text-base font-semibold mr-2">
                  Rp. {{ product.price }}
                </p>
                <router-link
                  to="#"
                  class="bg-white px-2 py-1 md:px-2 md:py-1 lg:px-4 lg:py-2 xl:px-4 xl:py-2 text-xs sm:text-xs md:text-xs lg:text-md xl:text-md rounded-sm text-slate-800 hover:text-slate-900 hover:bg-gray-200 font-semibold ml-2">
                  Details
                </router-link>
              </div>
            </div>
          </Slide>
        </Carousel>
      </div>
      <div class="flex mx-20">
        <!-- Second Carousel -->
        <Carousel
          :itemsToShow="3.7"
          :wrapAround="true"
          :transition="1000"
          :autoplay="4000"
          class="overflow-hidden">
          <!-- Products for the first carousel -->
          <Slide
            v-for="(product, index) in products"
            :key="index"
            class="-mx-2">
            <div class="font-quicksand mt-10 mx-5 text-left w-[300px]">
              <img
                :src="product.image"
                class="w-full h-64 object-cover mb-4"
                alt="Product Image" />
              <div class="px-4">
                <div
                  class="font-bold text-base md:text-xs lg:text-lg mb-2 text-gray-900 overflow-hidden">
                  {{ product.name }}
                  <p
                    class="text-gray-700 text-sm md:text-xs lg:text-md h-4 font-medium">
                    Pruduct Category - From Korea
                  </p>
                </div>

                <p
                  class="text-gray-700 text-sm md:text-xs lg:text-md h-4 mb-4 overflow-y-auto">
                  Description
                </p>
              </div>
              <div
                class="px-2 py-2 sm:px-2 sm:py-2 md:px-2 md:py-2 lg:px-4 lg:py-4 flex justify-between items-center bg-slate-800">
                <p
                  class="text-white text-xs sm:text-xs md:text-xs lg:text-md xl:text-base font-semibold mr-2">
                  Rp. {{ product.price }}
                </p>
                <router-link
                  to="#"
                  class="bg-white px-2 py-1 md:px-2 md:py-1 lg:px-4 lg:py-2 xl:px-4 xl:py-2 text-xs sm:text-xs md:text-xs lg:text-md xl:text-md rounded-sm text-slate-800 hover:text-slate-900 hover:bg-gray-200 font-semibold ml-2">
                  Details
                </router-link>
              </div>
            </div>
          </Slide>
        </Carousel>
      </div>
    </div>

    <div class="mt-20 bg-slate-800 py-12">
      <div class="container mx-auto px-4">
        <h2
          class="text-3xl tracking-widest font-switzer text-left mb-8 text-white">
          Testimonials
        </h2>
        <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-8">
          <!-- Testimonial 1 -->
          <div class="bg-white p-6 rounded-lg shadow-md">
            <p class="text-gray-800 text-base">
              "The product is amazing! It made my skin glow and feel so soft."
            </p>
            <div class="flex items-center mt-4">
              <img
                class="h-10 w-10 rounded-full mr-4"
                src="https://source.unsplash.com/random/50x50?face&sig=1"
                alt="testimonial" />
              <div>
                <p class="text-gray-900 font-semibold">Anna Williams</p>
                <p class="text-gray-600">Beauty Enthusiast</p>
              </div>
            </div>
          </div>

          <!-- Testimonial 2 -->
          <div class="bg-white p-6 rounded-lg shadow-md">
            <p class="text-gray-800 text-base">
              "I've never felt more confident in my skin. This product is a
              game-changer."
            </p>
            <div class="flex items-center mt-4">
              <img
                class="h-10 w-10 rounded-full mr-4"
                src="https://source.unsplash.com/random/50x50?face&sig=2"
                alt="testimonial" />
              <div>
                <p class="text-gray-900 font-semibold">Michael Lee</p>
                <p class="text-gray-600">Entrepreneur</p>
              </div>
            </div>
          </div>

          <!-- Testimonial 3 -->
          <div class="bg-white p-6 rounded-lg shadow-md">
            <p class="text-gray-800 text-base">
              "I can see a significant difference in my skin tone and texture.
              Highly recommend it!"
            </p>
            <div class="flex items-center mt-4">
              <img
                class="h-10 w-10 rounded-full mr-4"
                src="https://source.unsplash.com/random/50x50?face&sig=3"
                alt="testimonial" />
              <div>
                <p class="text-gray-900 font-semibold">Sophia Gomez</p>
                <p class="text-gray-600">Professional Photographer</p>
              </div>
            </div>
          </div>

          <!-- Testimonial 4 -->
          <div class="bg-white p-6 rounded-lg shadow-md">
            <p class="text-gray-800 text-base">
              "A must-have product! It made my skin look so vibrant and
              healthy."
            </p>
            <div class="flex items-center mt-4">
              <img
                class="h-10 w-10 rounded-full mr-4"
                src="https://source.unsplash.com/random/50x50?face&sig=4"
                alt="testimonial" />
              <div>
                <p class="text-gray-900 font-semibold">James Anderson</p>
                <p class="text-gray-600">Marketing Executive</p>
              </div>
            </div>
          </div>

          <!-- Testimonial 5 -->
          <div class="bg-white p-6 rounded-lg shadow-md">
            <p class="text-gray-800 text-base">
              "I've tried many products, but this one stands out. It's simply
              amazing!"
            </p>
            <div class="flex items-center mt-4">
              <img
                class="h-10 w-10 rounded-full mr-4"
                src="https://source.unsplash.com/random/50x50?face&sig=5"
                alt="testimonial" />
              <div>
                <p class="text-gray-900 font-semibold">Emma Thompson</p>
                <p class="text-gray-600">Writer</p>
              </div>
            </div>
          </div>

          <!-- Testimonial 6 -->
          <div class="bg-white p-6 rounded-lg shadow-md">
            <p class="text-gray-800 text-base">
              "My skin feels refreshed and rejuvenated after using this product.
              Highly recommended!"
            </p>
            <div class="flex items-center mt-4">
              <img
                class="h-10 w-10 rounded-full mr-4"
                src="https://source.unsplash.com/random/50x50?face&sig=6"
                alt="testimonial" />
              <div>
                <p class="text-gray-900 font-semibold">Olivia Carter</p>
                <p class="text-gray-600">Makeup Artist</p>
              </div>
            </div>
          </div>

          <!-- Testimonial 7 -->
          <div class="bg-white p-6 rounded-lg shadow-md">
            <p class="text-gray-800 text-base">
              "This product transformed my skincare routine! I can't go a day
              without it now."
            </p>
            <div class="flex items-center mt-4">
              <img
                class="h-10 w-10 rounded-full mr-4"
                src="https://source.unsplash.com/random/50x50?face&sig=7"
                alt="testimonial" />
              <div>
                <p class="text-gray-900 font-semibold">Lucas Martin</p>
                <p class="text-gray-600">Fashion Blogger</p>
              </div>
            </div>
          </div>

          <!-- Testimonial 8 -->
          <div class="bg-white p-6 rounded-lg shadow-md">
            <p class="text-gray-800 text-base">
              "I love how this product makes my skin look and feel. Absolutely
              recommend it!"
            </p>
            <div class="flex items-center mt-4">
              <img
                class="h-10 w-10 rounded-full mr-4"
                src="https://source.unsplash.com/random/50x50?face&sig=8"
                alt="testimonial" />
              <div>
                <p class="text-gray-900 font-semibold">Grace Park</p>
                <p class="text-gray-600">Software Engineer</p>
              </div>
            </div>
          </div>

          <!-- Testimonial 9 -->
          <div class="bg-white p-6 rounded-lg shadow-md">
            <p class="text-gray-800 text-base">
              "This product has transformed my skincare routine! My skin has
              never looked better."
            </p>
            <div class="flex items-center mt-4">
              <img
                class="h-10 w-10 rounded-full mr-4"
                src="https://source.unsplash.com/random/50x50?face&sig=9"
                alt="testimonial" />
              <div>
                <p class="text-gray-900 font-semibold">Lisa Kim</p>
                <p class="text-gray-600">Marketing Manager</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Section Carousel Pengiriman -->
    <div class="mt-10 py-12 mx-20 h-[500px]">
      <div class="container px-4">
        <h2 class="text-3xl tracking-widest font-switzer mb-20">* Shipping</h2>
        <Carousel
          :itemsToShow="4"
          :wrapAround="true"
          :transition="1000"
          :autoplay="true"
          :autoplayInterval="5000"
          class="overflow-hidden">
          <!-- Slides untuk layanan pengiriman -->
          <Slide
            v-for="(deliveryService, index) in deliveryServices"
            :key="index"
            class="px-2">
            <div class="flex items-center justify-center">
              <img
                :src="deliveryService.logo"
                alt="Logo Layanan Pengiriman"
                class="h-36" />
            </div>
          </Slide>
        </Carousel>
      </div>
    </div>

    <!-- Footer Section -->
    <div>
      <FooterVue />
    </div>
  </div>
</template>

<script>
import "animate.css";
import NavbarHome from "@/components/NavbarHome.vue";
import FooterVue from "../components/Footer.vue";
import "vue3-carousel/dist/carousel.css";

import { Carousel, Slide } from "vue3-carousel";

export default {
  name: "HomeView",
  components: {
    Carousel,
    Slide,
    NavbarHome,
    FooterVue,
  },
  data() {
    return {
      products: [
        {
          id: 1,
          name: "Product 1",
          image: "https://source.unsplash.com/random/300?cosmetic&sig=1",
          price: 1000000,
        },
        {
          id: 2,
          name: "Product 2",
          image: "https://source.unsplash.com/random/300?cosmetic&sig=2",
          price: 1500000,
        },
        {
          id: 3,
          name: "Product 3",
          image: "https://source.unsplash.com/random/300?cosmetic&sig=3",
          price: 800000,
        },
        {
          id: 4,
          name: "Product 4",
          image: "https://source.unsplash.com/random/300?cosmetic&sig=4",
          price: 1200000,
        },
        // Add more products as needed
      ],
      promotions: [
        {
          title: "20% Off Weekend Sale",
          description:
            "Get 20% off on all products this weekend! Use code: WEEKEND20. Hurry, offer ends soon!",
          image: "https://via.placeholder.com/300",
        },
        {
          title: "Newsletter Signup Discount",
          description:
            "Sign up for our newsletter and receive a $10 discount on your first purchase!",
          image: "https://via.placeholder.com/300",
        },
      ],
      deliveryServices: [
        {
          name: "SAP Express",
          logo: "https://www.sap-express.id/assets/img/logo/sapx-logo-og-image.png",
        },
        {
          name: "Arahin Id",
          logo: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRTRj4boMvd_B2bNbBQLZ-TrSfilRqjgwZQOEEtryqMug&s",
        },
        {
          name: "JNT Express",
          logo: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQn4suisXsn-dIb5bUs-CjpwlaGN1j7A8EaqKM5tz_Tkl5GEvO6qzokpcJ9vmeoumG0tEw&usqp=CAU",
        },
        {
          name: "JNE Express",
          logo: "https://cfstg.alfacart.com/media/revamp/mweb/assets/img/JNE.png",
        },
      ],
    };
  },
};
</script>

<style scoped>
/* * {
  border: red 1px solid;
} */
</style>
