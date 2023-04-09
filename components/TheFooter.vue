<template>
    <footer class="footer">
        <div class="container">
            <div class="row">
                <div class="col-sm-12 col-md-3 col-lg-3">
                    <img class="img-fluid logo-footer" src="@/assets/images/logo-ecolify-putih.svg" alt="Logo Ecolify">
                    <img class="img-fluid" src="@/assets/images/logo.svg" alt="Logo LindungiHutan">
                    <p class="footer__desc mt-1">
                        <span class="fw-bold">Ecolify</span>
                        adalah platform yang memudahkan organisasi, instansi dan perusahaan untuk menjalankan projek sosial penanaman pohon secara transparan dan berkelanjutan.
                    </p>
                </div>
                <div class="col-sm-12 col-md-2 col-lg-2">
                    <ul class="mt-2">
                        <h5 class="title fw-bold">Peta Situs</h5>
                        <li class="list">Beranda</li>
                        <li class="list">Blog</li>
                        <li class="list">Kenapa</li>
                        <li class="list">Lokasi</li>
                        <li class="list">Layanan</li>
                    </ul>
                </div>
                <div class="col-sm-12 col-md-2 col-lg-2">
                    <ul class="mt-2">
                        <h5 class="title fw-bold">Resources</h5>
                        <li class="list">FAQ</li>
                        <li class="list">Kebijakan Privasi</li>
                    </ul>
                </div>
                <div class="col-sm-12 col-md-3 col-lg-3">
                    <ul class="mt-2">
                        <h5 class="title fw-bold">Hubungi Kami</h5>
                        <li class="list fw-semibold">
                            email: <br>
                            <span class="fw-light">kartika[at]lindungihutan.com</span>
                        </li>
                        <li class="list fw-semibold mt-2">
                            wa/phone: <br>
                            <span class="fw-light">+62 813 2918 1389</span>
                        </li>
                        <li class="list fw-semibold mt-2">
                            location: <br>
                            <span class="fw-light">Jalan Lempongsari 1 No. 405, Semarang, Indonesia</span></li>
                        <li class="list fw-semibold mt-2">
                            legal info: <br>
                            <span class="fw-light">Keputusan MENKUMHAM NOMOR AHU-0003033.AHA.01.04.</span>
                        </li>
                    </ul>
                </div>
                <div class="col-sm-12 col-md-2 col-lg-2">
                    <ul class="mt-2">
                        <h5 class="title fw-bold">Ikuti Kami</h5>
                        <li class="icon-list">
                            <img class="img-fluid img-social" src="@/assets/images/twitter.svg" alt="Logo Twitter">
                            <img class="img-fluid img-social" src="@/assets/images/linkedin.svg" alt="Logo Twitter">
                            <img class="img-fluid img-social" src="@/assets/images/medium.svg" alt="Logo Twitter">
                        </li>
                    </ul>
                </div>
            </div>
            <div class="row footer__copyright">
                <p>LindungiHutan &copy; 2020 - made with conscience "for a future worth living"</p>
            </div>
        </div>
    </footer>
</template>

<style lang="scss" scoped>
.footer {
    background-color: #47BAA6;
    color: #ffffff;

    .logo-footer {
        max-width: 150px;
    }

    &__desc {
        font-size: 14px;
    }

    .title {
        font-size: 18px;
    }

    .list {
        list-style: none;

        span {
            font-size: 14px;
        }
    }

    .icon-list {
        display: flex;
        flex-direction: row;
        gap: 10px;
    }

    .img-social {
        max-width: 30px;
    }

    &__copyright {
        font-size: 14px;
    }
}
</style>