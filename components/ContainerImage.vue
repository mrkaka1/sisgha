<template>
    <div>
        <div id="drop-area" @drop="dropHandler" @dragover.prevent="dragOverHandler">
            <svg class="newImage" width="50" height="50" viewBox="0 0 41 41" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path
                    d="M5.66025 34.0272H30.3669C32.3884 34.0272 34.0272 32.3884 34.0272 30.3669V5.66025C34.0272 3.63875 32.3884 2 30.3669 2H5.66025C3.63875 2 2 3.63875 2 5.66025V30.3669C2 32.3884 3.63875 34.0272 5.66025 34.0272Z"
                    stroke="#ADADAD" stroke-width="2.17143" />
                <path
                    d="M5.72878 32.9291L5.68316 33.4257C5.49826 35.4388 6.98026 37.2205 8.99328 37.4054L33.5964 39.6652C35.6094 39.8501 37.3912 38.3681 37.5761 36.3551L39.8358 11.752C40.0207 9.73895 38.5387 7.95718 36.5257 7.77229L35.1586 7.64672"
                    stroke="#ADADAD" stroke-width="2.17143" stroke-linecap="round" stroke-dasharray="3.66 3.66" />
                <path
                    d="M17.4645 25.6543L11.0929 20.5868C10.2942 19.9516 9.13013 20.0924 8.50588 20.8998L2 29.3146V30.3669C2 32.3884 3.63875 34.0272 5.66025 34.0272H30.3669C32.3884 34.0272 34.0272 32.3884 34.0272 30.3669V23.4582L27.0054 15.428C26.2102 14.5186 24.7678 14.6154 24.1013 15.6228L17.4645 25.6543Z"
                    fill="#ADADAD" />
                <path
                    d="M15.7717 12.6605C15.1147 12.0035 14.0495 12.0035 13.3925 12.6605C12.7355 13.3175 12.7355 14.3826 13.3925 15.0396C14.0495 15.6966 15.1147 15.6966 15.7717 15.0396C16.4287 14.3826 16.4287 13.3175 15.7717 12.6605Z"
                    fill="#ADADAD" />
            </svg>

            <div class="ctt">
                Arraste e solte uma imagem ou escolha uma de até 500 KB .jpeg ou .png
            </div>
            <input type="file" ref="fileInput" @change="handleFile" accept=".jpeg, .jpg, .png" />
        </div>
        <div v-if="imageSrc">
            <img :src="imageSrc" alt="Imagem carregada" />
        </div>
    </div>
</template>

<script setup>
const data = ref({
    imageSrc: null,
});

const dropHandler = (event) => {
    event.preventDefault();
    handleFiles(event.dataTransfer.files);
};

const dragOverHandler = (event) => {
    event.preventDefault();
};

const handleFile = () => {
    const fileInput = refs.fileInput;
    handleFiles(fileInput.files);
};

const handleFiles = (files) => {
    const file = files[0];

    if (
        file &&
        (file.type === "image/jpeg" || file.type === "image/png") &&
        file.size <= 500 * 1024
    ) {
        const reader = new FileReader();

        reader.onload = (e) => {
            data.imageSrc = e.target.result;
        };

        reader.readAsDataURL(file);
    } else {
        alert(
            "Por favor, escolha uma imagem válida de até 500 KB nos formatos .jpeg ou .png."
        );
    }
};
</script>

<style scoped>
#drop-area {
    width: 380px;
    height: 200px;
    border: 2px solid #9ab69e;
    border-radius: 8px;
    text-align: center;
    margin: 50px auto;
    cursor: pointer;
}

#drop-area input[type="file"] {
    display: none;
}

#drop-area img {
    max-width: 100%;
    max-height: 100%;
}

.newImage {
    margin-top: 40px;
    margin-left: 168px;
}

.ctt {
    margin-top: 20px;
    font-weight: 500;
    color: #ADADAD;
}
</style>
