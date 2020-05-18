<template>
    <section class="product center">
        <div class="product-header">
            <h1 class="product-h1">Fetured Items</h1>
            <h3 class="product-h3">Shop for items based on what we featured in this week</h3>
        </div>
        <div class="product-items">
            <SimpleProduct v-for="item of filtered"
                           :key="item.id_product"
                           :img="item.img"
                           :product="item">
            </SimpleProduct>
        </div>
        <div class="button-prod-div">
            <a class="button button-product" href="product.html">Browse All Product <img alt="arrow" class="arrow"
                                                                                         src="img/arrow-right.png"></a>
        </div>
    </section>
</template>

<script>
    import SimpleProduct from "../../ProductProto/SimpleProduct";

    export default {
        name: "MainProduct",
        components: {SimpleProduct},
        data() {
            return {
                filtered: [
                    {
                        "id_product": 1,
                        "product_name": "MANGO PEOPLE T-SHIRT",
                        "price": 50,
                        "img": '/img/product-item-1.png'
                    },
                    {
                        "id_product": 2,
                        "product_name": "MANGO PEOPLE T-SHIRT",
                        "price": 150,
                        "img": '/img/product-item-2.png'
                    },
                    {
                        "id_product": 3,
                        "product_name": "MANGO PEOPLE T-SHIRT",
                        "price": 70,
                        "img": '/img/product-item-3.png'
                    },
                    {
                        "id_product": 4,
                        "product_name": "MANGO PEOPLE T-SHIRT",
                        "price": 590,
                        "img": '/img/product-item-4.png'
                    },
                    {
                        "id_product": 5,
                        "product_name": "MANGO PEOPLE T-SHIRT",
                        "price": 159,
                        "img": '/img/product-item-5.png'
                    },
                    {
                        "id_product": 6,
                        "product_name": "MANGO PEOPLE T-SHIRT",
                        "price": 170,
                        "img": '/img/product-item-6.png'
                    },
                    {
                        "id_product": 7,
                        "product_name": "MANGO PEOPLE T-SHIRT",
                        "price": 501,
                        "img": '/img/product-item-7.png'
                    },
                    {
                        "id_product": 8,
                        "product_name": "MANGO PEOPLE T-SHIRT",
                        "price": 15,
                        "img": '/img/product-item-8.png'
                    },
                ]
            }
        }
    }
</script>

<style>
    .prod-item-height {
        width: 261px;
        margin-top: 50px;
        position: relative;
    }

    .prod-item-height:hover .prod-img {
        transition-duration: 0.5s;
        filter: brightness(50%);
    }

    .prod-item-height:hover .product-add, .prod-item-height:hover .product-add-prod-r, .prod-item-height:hover .product-add-prod-l {
        transition-duration: 0.5s;
        display: flex;
    }

    .product-add, .product-add-prod-r, .product-add-prod-l {
        position: absolute;
        top: 97px;
        left: 70px;
        height: 39px;
        width: 123px;
        border: 1px solid white;
        display: none;
        justify-content: center;
        align-items: center;
        font-size: 13px;
        font-weight: bold;
        color: white;
    }

    .product-add-prod-l {
        width: 57px;
        top: 144px;
    }

    .product-add-prod-r {
        width: 57px;
        top: 144px;
        left: 136px;
        transition: all;
        transition-duration: 0.2s;
    }

    .product-add:hover, .product-add-prod-l:hover, .product-add-prod-r:hover {
        box-shadow: 0 0 5px #fff;
    }

    .product-add img, .product-add-prod-l img, .product-add-prod-r img {
        margin-right: 5px;
    }

    .product-header {
        text-align: center;
        font-size: 14px;
        font-weight: bold;
        color: #222222;
        letter-spacing: 0.03em;
    }

    .product-h1 {
        font-size: 30px;
        font-weight: bold;
        color: #222222;
        letter-spacing: 0.03em;
    }

    .product-h3 {
        color: #9f9f9f;
    }

    .product-items {
        display: flex;
        flex-wrap: wrap;
        justify-content: space-between;
    }

    .prod-link {
        display: flex;
    }

    .product-item-1, .product-item-2, .product-item-3,
    .product-item-4, .product-item-5, .product-item-6,
    .product-item-7, .product-item-8 {
        background-repeat: no-repeat;
    }

    .product-item-1 {
        margin-left: 0;
        background-image: url(/public/img/product-item-1.png);
    }

    .product-item-2 {
        background-image: url(/public/img/product-item-2.png);
    }

    .product-item-3 {
        background-image: url(/public/img/product-item-3.png);
    }

    .product-item-4 {
        background-image: url(/public/img/product-item-4.png);
    }

    .product-item-5 {
        margin-left: 0;
        background-image: url(/public/img/product-item-5.png);
    }

    .product-item-6 {
        background-image: url(/public/img/product-item-6.png);
    }

    .product-item-7 {
        background-image: url(/public/img/product-item-7.png);
    }

    .product-item-8 {
        background-image: url(/public/img/product-item-8.png);
    }

    .product-text, .product-price {
        margin: 18px;
        font-size: 14px;
        color: #6f6e6e;
        text-transform: uppercase;
    }

    .product-price {
        font-size: 16px;
        font-weight: bold;
        color: #f16d7f;
    }

    .button-prod-div {
        display: flex;
        justify-content: center;
    }

    .button-product {
        margin-top: 79px;
        padding: 5px 18px;
        display: flex;
        justify-content: center;
        align-items: center;
        background-color: #f16d7f;
        font-size: 15px;
        font-weight: 300;
        color: #fff;
        letter-spacing: 0.03em;
        transition: all;
        transition-duration: 0.2s;
    }

    .button-product:hover {
        box-shadow: 0 0 15px 5px rgba(0, 0, 0, 0.17);
    }
</style>