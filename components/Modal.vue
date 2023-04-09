<template>
    <div class="modal fade" id="exampleModal" tabindex="-1" aria-labelledby="exampleModalLabel" aria-hidden="true">
        <div class="modal-dialog">
            <div class="modal-content">
                <div class="modal-body">
                    <div class="text-center mb-5">
                        <h5 class="modal-title" id="exampleModalLabel">Get our pitchdeck to know why <br> Ecolify doing better</h5>
                    </div>
                    <label for="input-name" class="form-label">Name</label>
                    <div class="input-group mb-3">
                        <input id="input-name" type="text" class="form-control form-input" placeholder="Enter your name">
                    </div>
                    <label for="input-email" class="form-label">Email</label>
                    <div class="input-group mb-3">
                        <input id="input-email" type="email" class="form-control form-input" placeholder="Enter your email">
                    </div>
                    <div class="text-center mt-4">
                        <BaseButton :isPrimary="false" :isSmallButton="true" padding="12px 25px" name="Download" />
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.modal-content {
    padding: 20px 40px;

    .modal-title {
        font-weight: 600;
        color: #212322;
    }
}

.form-input {
    height: 48px;
    border-radius: 15px;
}
</style>