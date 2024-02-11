<template >
    <footer>
        <div class="container">
            <div class="footer_wrapper">
                <div class="footer_top">
                    <div class="footer_logo">
                        <img src="../assets/icons/footerlogo.svg" alt="footerlogo.svg">
                    </div>
                    <div class="contact">
                        <div class="contact_item">
                            <p>Email</p>
                            <a href="#">info@tpm.house</a>
                        </div>
                        <div class="phone contact_item">
                            <p>Phone</p>
                            <a href="tel:+998943330799">+998943330799</a>
                        </div>
                        <div class="contact_item">
                            <p>Address</p>
                            <a href="#">Toshkent sh. Yunusobod tumani, Bogishamol 105</a>
                        </div>
                    </div>
                </div>
                <div class="footer_bottom">
                    <p>© 2023 TPM, All rights reserved</p>
                    <div class="footer_bottom-right">
                        <p>Terms of Use</p>
                        <p>Privacy policy</p>
                        <div class="footer_bottom-right_img">
                            <img src="../assets/icons/footergoogleplay.svg" alt="footergoogleplay.svg">
                            <img src="../assets/icons/footerappstire.svg" alt="footerappstire.svg">
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </footer>
</template>

<script setup>

</script>

<style scoped>
footer {
    border-bottom: 1px solid var(--system-colors-gray-700, #2F3641);
    background: var(--system-colors-gray-800, #1C232C);
    padding: 30px 0px;
}

.footer_top {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding-bottom: 30px;

}

.contact {
    display: flex;
    align-items: center;
    gap: 32px;
}

/* #2F3641 */
.contact .contact_item {
    padding: 0px 60px;
}

.contact .phone {
    padding: 0px 60px 0px 0px;
}

.contact div:not(:last-child) {
    border-right: 1px solid var(--system-colors-gray-700, #2F3641);
}

.contact div p {
    color: var(--black-white-white, #FFF);
    font-size: 20px;
    font-weight: 500;
}

.contact div a {
    color: var(--black-white-white, #FFF);
    font-size: 16px;
    font-weight: 500;
}

.footer_bottom {
    display: flex;
    align-items: center;
    justify-content: space-between;
}

.footer_bottom-right {
    display: flex;
    align-items: center;
    gap: 32px;
}

.footer_bottom p {
    color: var(--system-colors-gray-500, #636C79);
    font-size: 16px;
    font-weight: 500;
    line-height: 32px;
}
.footer_bottom-right_img{
    display: flex;
    align-items: center;
    gap: 20px;
}
@media screen and (max-width:992px){
    
}
</style>