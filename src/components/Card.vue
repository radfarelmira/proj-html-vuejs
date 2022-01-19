<template>
    <div class="col">
        <div class="card">
            <img :src="detailes.src" class="card-img-top" alt="...">
            <div class="card-body">
                <div class="title">{{detailes.title}}</div>
                <p class="card-text">{{detailes.text}}</p>
                <div class="parches-info">
                    <div>
                        <i v-for="n in starRating" :key="n" id="raiting-star" class="fas fa-star"></i> 
                        <i v-for="n in (maxStarRating - starRating)" :key="n" id="fas-star" class="fas fa-star"></i>
                    </div>

                    <div class="price">
                        <div class="ex-price">{{detailes.exPrice}}</div>
                        <div class="discount">{{detailes.discount}}</div>
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
            maxStarRating: 5,
            starRating: 0
        }; 
    },
    methods: {
        getRaiting: function(){
            return this.starRating = parseInt(this.detailes.raiting)    
        }
    },
    created: function(){
        this.getRaiting()
    }

}
</script>

<style scoped lang="scss">

.col{
    
    .card{
        text-align: left;
        transition: transform .2s;

        .card-body{

            .title{
                font-size: 14px;
                color: lightgray;
            }

            p{
                min-height: 120px;
                font-size: 16px;
                border-bottom: 1px solid lightgray;
                padding: 10px 0;
            }

            .parches-info{
                min-height: 35px;
                font-size: 12px;
                display: flex;
                justify-content: space-between;
                align-items: center;

                #fas-star{
                    color: lightgray;    
                }

                #raiting-star{
                    color: #f59d1a;
                }

                .price{
                    text-align: right;
                    
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