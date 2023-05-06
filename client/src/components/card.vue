<template>
    <div class="card">
        <img :src="url" :alt="alt">

        <div class="details">
            <div class="subdetails">
                <small> {{ category }} </small>
                <average></average>
            </div>
            <p><strong> {{ title }} </strong> </p>
            <div class="prices">
                <span> {{ price }}  </span>
                <s> {{ strikeprice }}  </s>
            </div>
        </div>

     <div>

        SelfPlaced
        <div class="svgStyle">

       
        <svg viewBox="0 -7 48 48" version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" fill="#000000"><g id="SVGRepo_bgCarrier" stroke-width="0"></g><g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g><g id="SVGRepo_iconCarrier"> <title>Youtube-color</title> <desc>Created with Sketch.</desc> <defs> </defs> <g id="Icons" stroke="none" stroke-width="1" fill="none" fill-rule="evenodd"> <g id="Color-" transform="translate(-200.000000, -368.000000)" fill="#CE1312"> <path d="M219.044,391.269916 L219.0425,377.687742 L232.0115,384.502244 L219.044,391.269916 Z M247.52,375.334163 C247.52,375.334163 247.0505,372.003199 245.612,370.536366 C243.7865,368.610299 241.7405,368.601235 240.803,368.489448 C234.086,368 224.0105,368 224.0105,368 L223.9895,368 C223.9895,368 213.914,368 207.197,368.489448 C206.258,368.601235 204.2135,368.610299 202.3865,370.536366 C200.948,372.003199 200.48,375.334163 200.48,375.334163 C200.48,375.334163 200,379.246723 200,383.157773 L200,386.82561 C200,390.73817 200.48,394.64922 200.48,394.64922 C200.48,394.64922 200.948,397.980184 202.3865,399.447016 C204.2135,401.373084 206.612,401.312658 207.68,401.513574 C211.52,401.885191 224,402 224,402 C224,402 234.086,401.984894 240.803,401.495446 C241.7405,401.382148 243.7865,401.373084 245.612,399.447016 C247.0505,397.980184 247.52,394.64922 247.52,394.64922 C247.52,394.64922 248,390.73817 248,386.82561 L248,383.157773 C248,379.246723 247.52,375.334163 247.52,375.334163 L247.52,375.334163 Z" id="Youtube"> </path> </g> </g> </g></svg>
    </div>
    </div>

        <svg @click="fillsvg" width="18" height="18" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
            <path :fill-rule="like" clip-rule="evenodd"
                d="M12.0122 5.57169L10.9252 4.48469C8.77734 2.33681 5.29493 2.33681 3.14705 4.48469C0.999162 6.63258 0.999162 10.115 3.14705 12.2629L11.9859 21.1017L11.9877 21.0999L12.014 21.1262L20.8528 12.2874C23.0007 10.1395 23.0007 6.65711 20.8528 4.50923C18.705 2.36134 15.2226 2.36134 13.0747 4.50923L12.0122 5.57169ZM11.9877 18.2715L16.9239 13.3352L18.3747 11.9342L18.3762 11.9356L19.4386 10.8732C20.8055 9.50635 20.8055 7.29028 19.4386 5.92344C18.0718 4.55661 15.8557 4.55661 14.4889 5.92344L12.0133 8.39904L12.006 8.3918L12.005 8.39287L9.51101 5.89891C8.14417 4.53207 5.92809 4.53207 4.56126 5.89891C3.19442 7.26574 3.19442 9.48182 4.56126 10.8487L7.10068 13.3881L7.10248 13.3863L11.9877 18.2715Z"
                fill="red" />
        </svg>


        <button class="cart" @click="add_to_cart()">
            <svg width="18" height="18" viewBox="0 0 24 24" fill="white" xmlns="http://www.w3.org/2000/svg">
                <path fill-rule="evenodd" clip-rule="evenodd"
                    d="M5 4H19C19.5523 4 20 4.44771 20 5V19C20 19.5523 19.5523 20 19 20H5C4.44772 20 4 19.5523 4 19V5C4 4.44772 4.44771 4 5 4ZM2 5C2 3.34315 3.34315 2 5 2H19C20.6569 2 22 3.34315 22 5V19C22 20.6569 20.6569 22 19 22H5C3.34315 22 2 20.6569 2 19V5ZM12 12C9.23858 12 7 9.31371 7 6H9C9 8.56606 10.6691 10 12 10C13.3309 10 15 8.56606 15 6H17C17 9.31371 14.7614 12 12 12Z"
                    fill="white" />
            </svg>



        </button>
        <button class="compare" @click="add_to_compare()">
            <!-- <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <path d="M16 13V11.5H10V9.5H16V8L19 10.5L16 13Z" fill="white" />
                            <path d="M8 17V15.5H14V13.5H8V12L5 14.5L8 17Z" fill="white" />
                        </svg> -->


                        <svg viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg" fill="#000000"><g id="SVGRepo_bgCarrier" stroke-width="0"></g><g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g><g id="SVGRepo_iconCarrier"> <rect x="0" fill="none" width="20" height="20"></rect> <g> <path d="M11 7H9.49c-.63 0-1.25.3-1.59.7L7 5H4.13l-2.39 7h1.69l.74-2H7v4H2c-1.1 0-2-.9-2-2V5c0-1.1.9-2 2-2h7c1.1 0 2 .9 2 2v2zM6.51 9H4.49l1-2.93zM10 8h7c1.1 0 2 .9 2 2v7c0 1.1-.9 2-2 2h-7c-1.1 0-2-.9-2-2v-7c0-1.1.9-2 2-2zm7.25 5v-1.08h-3.17V9.75h-1.16v2.17H9.75V13h1.28c.11.85.56 1.85 1.28 2.62-.87.36-1.89.62-2.31.62-.01.02.22.97.2 1.46.84 0 2.21-.5 3.28-1.15 1.09.65 2.48 1.15 3.34 1.15-.02-.49.2-1.44.2-1.46-.43 0-1.49-.27-2.38-.63.7-.77 1.14-1.77 1.25-2.61h1.36zm-3.81 1.93c-.5-.46-.85-1.13-1.01-1.93h2.09c-.17.8-.51 1.47-1 1.93l-.04.03s-.03-.02-.04-.03z"></path> </g> </g></svg>
        </button>
        
    </div>
</template>
    
<script setup>
import { ref } from 'vue';
import average from './average.vue';

defineProps({
    url: {
        type: String,
        required: true,
    },
    alt: {
        type: String,
        required: true,
    },
    title: {
        type: String,
        required: true,
    },
    category: {
        type: String,
        required: true,
    },
    price: {
        type: Number,
        required: true,
    },
    strikeprice: {
        type: Number,
        default: 0,
    },
})

const like = ref('evenodd')
const fillsvg = () => {
    if (like.value === '' ) {
        like.value = 'evenodd'
        send_something_to_content('dis_like')
    }
    else {
        like.value = ''
        send_something_to_content('handle_like')
    }
}
const add_to_cart = () => {
    send_something_to_content('item_clicked')
}
const send_something_to_content = defineEmits(['handle_like', 'dis_like', 'item_clicked'])

</script>
    
<style scoped>
.card {
    background-color: white;
    border: 1px solid transparent;
    border-radius: 10px;
    padding: 30px;
    margin: 10px;
    position: relative;
}

small {
    color: gray;
}

img {
    width: 100%;
    height: 300px;
    margin-bottom: 10px;
}

.details {
    border-top: 1px solid #ccc;
}
.details strong {
    font-size: 1.1em;
}
.details p {
    width: 60%;
}
.subdetails {
    display: grid;
    grid-template-columns: 1fr 1fr;
}
.prices span {
    font-weight: bold;
    font-size: 1.5em;
}

strike {
    color: gray;
}

.cart {
    cursor: pointer;
    position: absolute;
    bottom: 15px;
    right: 15px;
    width: 50px;
    height: 50px;
    border: 1px solid #ccc;
    border-radius: 50%;
    background-color: var(--secondary);
}
.compare {
    cursor: pointer;
    position: absolute;
    bottom: 15px;
    right: 75px;
    width: 50px;
    height: 50px;
    border:  #fff;
    border-radius: 50%;
    /* background-color: var(--secondary); */
}
.svgStyle{
    width: 28px;
}

</style>