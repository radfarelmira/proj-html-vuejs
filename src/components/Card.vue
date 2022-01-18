<template>
    <div class="col">
        <div class="card">
            <img :src="detailes.src" class="card-img-top" alt="...">
            <div class="card-body">
                <div class="title">Development ></div>
                <p class="card-text">{{detailes.text}}</p>
                <div class="parches-info">
                    <div>
                        <i v-for="n in starRating" :key="n" id="yellow" class="fas fa-star"></i>

                        <i id="gray" class="fas fa-star"></i>
                    </div>

                    <div class="price">
                        <div class="ex-price">$199.99</div>
                        <div class="discount">$50</div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Card',
    props:{
        detailes: Object,
    },
    data: function(){
        return{
            starRating: 4,
        }; 
    }

}
</script>

<style scoped lang="scss">

.col{

    .card{

        .card-body{

            .title{
                font-size: 14px;
                color: lightgray;
            }

            p{
                font-size: 16px;
                border-bottom: 1px solid lightgray;
                padding: 10px 0;
            }

            .parches-info{
                font-size: 12px;
                display: flex;
                justify-content: space-between;
                align-items: center;

                #yellow{
                    color: #f59d1a;
                }

                #gray{
                    color: lightgray;
                }

                .price{

                    .ex-price{
                        text-decoration: line-through;
                        color: lightgray;
                    }

                    .discount{
                        font-weight: bold;
                    }
                }
            }
        }
    }
}


</style>