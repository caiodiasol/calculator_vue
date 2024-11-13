
<template>
    <footer class="footer text-center p-3">
        <ul class="social-icons list-unstyled d-flex justify-content-center mb-2">
            <li class="me-3">
                <a href="https://www.linkedin.com/in/caio-dias-de-oliveira-536797b2/" target="_blank" rel="noopener noreferrer">
                    <i class="bi bi-linkedin black-text pe-4"></i>
                </a>
            </li>
            <li>
                <a href="https://github.com/caiodiasol" target="_blank" rel="noopener noreferrer">
                    <i class="bi bi-github black-text pe-3"></i>
                </a>
            </li>
        </ul>
        <div>
            <p class="footer-text text-black ">
                ® 2024 - Caio Dias - All rights reserved.
            </p>
        </div>
    </footer>
</template>

<style scoped>
.footer{
    max-width: 400px;
    margin: 8px auto 0;
    border-radius: 10px;
    background-color: #f0f0f0;
    box-shadow: 1px 6px 12px rgba(0, 0, 0, 0.1);
    padding: 15px;
}

.black-text {
    color: #000;
}

li:hover {
    transform: scale(1.2);
    transition: 0.5s;
}
</style>