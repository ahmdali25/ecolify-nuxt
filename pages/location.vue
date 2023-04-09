<template>
    <div>
        <section class="container">
            <div class="row">
                <div class="col-sm-12 col-md-8 col-lg-8">
                    <h1 class="title fw-semibold">Temukan Lokasi</h1>
                    <h3 class="sub-title fw-light mt-4">Kami menanam pohon lebih dari 16 lokasi</h3>
                </div>
                <div class="col-sm-12 col-md-4 col-lg-4">
                    <select class="select">
                        <option value="" disabled selected>Pick based on area</option>
                        <option value="all">All Area</option>
                        <option value="dki">DKI Jakarta</option>
                        <option value="jabar">Jawa Barat</option>
                        <option value="jateng">Jawa Tengah</option>
                        <option value="jatim">Jawa Timur</option>
                        <option value="kalbar">Kalimantan Barat</option>
                        <option value="kalsel">Kalimantan Selatan</option>
                        <option value="ntb">Nusa Tenggara Barat</option>
                        <option value="riau">Riau</option>
                        <option value="sulsel">Sulawesi Selatan</option>
                        <option value="sulteng">Sulawesi Tengah</option>
                    </select>
                </div>
            </div>
        </section>
        <section class="container mt-5">
           <div class="row">
                <div class="col-12">
                    <h4 class="text-location">{{ locations.data.length }} Location</h4>
                </div>
           </div>
        </section>
        <section class="container mt-2">
           <div class="row">
            <div class="col-2">
                <div class="card-scroll">
                    <div class="card card-location" v-for="(location,index) in locations.data" :key="index">
                        <img class="card-img-top" :src="location.image" loading="lazy" alt="Kampung Laut Cilacap">
                        <div class="card-body">
                            <h6 class="card-title fw-bold text-center">{{ location.nama_lokasi }}<span v-if="location.kabupaten">,</span> <br> {{ location.kabupaten }}</h6>
                            <p class="card-text text-center">{{ location.provinsi }}</p>
                        </div>
                    </div>
                </div>
            </div>
            <div class="col-10">
                <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d16329410.491234343!2d108.3863817080079!3d-2.275399859669337!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x2c4c07d7496404b7%3A0xe37b4de71badf485!2sIndonesia!5e0!3m2!1sid!2sid!4v1680933795668!5m2!1sid!2sid"
                    width="100%"
                    height="400"
                    style="border:0;"
                    allowfullscreen
                    loading="lazy"
                    referrerpolicy="no-referrer-when-downgrade">
                </iframe>
            </div>
           </div>
        </section>
        <section class="container mt-4 mb-5">
            <div class="row justify-content-center">
                <h2 class="text-cta text-center mb-4">Punya lokasi lain untuk penanaman?</h2>
            <div class="text-center">
                <BaseButton :isPrimary="false" :isSmallButton="false" padding="10px 30px" name="Sarankan Kami" />
            </div>
            </div>
        </section>
        <section class="download-section">
            <div class="row justify-content-center">
                <div class="col-sm-12 col-md-6 col-lg-6">
                    <h4 class="download-section__title">Buat <span>Dampak</span> Nyata Sekarang</h4>
                    <p class="download-section__text mt-3">Silahkan pelajari kami lebih detail dengan mengunduh <br> pitchdeck kami</p>
                </div>
                <div class="col-sm-12 col-md-6 col-lg-6">
                    <div class="text-center">
                        <BaseButton :isPrimary="true" :isSmallButton="false" padding="6px 50px" name="Unduh" />
                    </div>
                </div>
            </div>
        </section>
    </div>
</template>

<script setup>
const { data: locations } = await useFetch("https://mocki.io/v1/eac0f512-e599-4ac4-8ed8-a0737f9cd138");
</script>

<style lang="scss">
.title {
    margin-top: 8%;
    font-size: 48px;
}

.sub-title {
    font-size: 24px;
}

.text-location {
    font-size: 18px;
    font-weight: 500;
    color: #212232;
}

.select {
    margin-top: 135px;
    border: none;
    background-color: #e5e5e5;
    color: #495057;
    border-radius: 6px;
    width: 100%;
    height: 22%;
    font-size: 1rem;
    font-weight: 400;
    line-height: 1.5;
    color: #495057;
    padding: 8px;
}

.card-body {
    padding: 10px;
}

.card-scroll {
    height: 400px;
    overflow-y: scroll;
    display: flex;
    flex-direction: column;
    gap: 20px;
    scrollbar-color: #2dc48d #d9fff1;
    scrollbar-width: 12px;
}

.card-scroll::-webkit-scrollbar {
  width: 12px;  /* width of the entire scrollbar */
}

.card-scroll::-webkit-scrollbar-track {
  background: #d9fff1;  /* color of the tracking area */
  border-radius: 20px; /* roundness of the tracking area */
}

.card-scroll::-webkit-scrollbar-thumb {
  background-color: #2DC48D;    /* color of the scroll thumb */
  border-radius: 20px;  /* roundness of the scroll thumb */
}

.card {
    width: 146px;
    box-shadow: 0 0.3rem 0.5rem rgba(0,0,0,.2);
    cursor: pointer;
}

.card-title {
    font-size: 12px;
}

.card-text {
    font-size: 12px;
}

.card-location {
    height: 140px;
}

.card-location:hover {
    text-decoration: underline;
}

.text-cta {
    font-size: 24px;
    font-weight: 600;
}

.download-section {
    background-color: #F5F5F5;
    padding: 60px 120px 120px;
    margin-bottom: -120px;
    color: #212232;

    &__title {
        font-size: 24px;
        font-weight: 700;
        margin-left: 120px;

        span {
            color: #2DC48D;
        }
    }

    &__text {
        margin-left: 120px;
        font-size: 14px;
    }
}
</style>