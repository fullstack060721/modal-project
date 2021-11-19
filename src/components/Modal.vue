<template>
    <div class="backdrop">
        <div class="modal">
            <h1>Modal header</h1>
            <p>modal content</p>
        </div>
    </div>
</template>
<style>

.modal {
    width: 400px;
    padding: 20px;
    margin: 100 px auto;
    background: gainsboro;
    border-radius :10 px;
}
.backdrop {
    top: 0;
    position: fixed;
    background: rgba (0, 0, 0, 0.5);
    width: 100%;
    height: 100%;
}
.modal h1 {
    color: #03cfb4;
    border: none;
    padding: 0;
}
.modal p {
    font-style: normal;
}
</style>