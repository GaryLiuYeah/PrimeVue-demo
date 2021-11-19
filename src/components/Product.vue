<template>
  <div class="product-content">
    <div class="product">
      <div class="imgs">
        <img src="../assets/img1.jpeg" alt="" />
      </div>
      <div class="detail">
        <div class="reverse-link">Charter Club</div>
        <div class="product-title">
          Patterned Wrap Scarf, Created for Macy's
        </div>
        <div class="web-id">Web ID: 12837302</div>
        <div class="stars">
          <i class="pi pi-star-fill"></i>
          <i class="pi pi-star-fill"></i>
          <i class="pi pi-star-fill"></i>
          <i class="pi pi-star-fill"></i>
          <i class="pi pi-star-fill grey-star"></i>
          <span>(2)</span>
        </div>
        <div class="legal">BLACK FRIDAY SPECIAL</div>
        <div class="price">
          <span class="red">$9.99</span>
          <span class="strike">$25.00</span>
          <span class="link-btn">Details</span>
        </div>
        <div class="link-btn">$29.99 Diamond Bonus Buy</div>
        <div class="color-wrap">
          <div><span class="bold">Color</span></div>
        </div>
        <p><span class="bold">Size:</span> ONE SIZE</p>
        <p class="bold">5,516 Customers Purchased</p>
        <button class="add-btn">Add To Bag</button>
        <div>
          <i class="pi pi-heart"></i>
          <span class="link-btn">Add To List</span>
        </div>
      </div>
    </div>
    <div class="carousel">
      <Carousel
        :value="products"
        :numVisible="3"
        :numScroll="3"
        orientation="vertical"
        verticalViewPortHeight="780px"
      >
        <template #header>
          <div class="bold">Customers also shopped</div>
        </template>
        <template #item="slotProps">
          <div class="product-item">
            <div class="product-img">
              <img :src="slotProps.data.img" alt="" />
            </div>
            <div class="product-info">
              <a href="#">
                <div class="bold">{{ slotProps.data.brand }}</div>
                <div class="product-name">${{ slotProps.data.name }}</div>
              </a>
              <div class="price">
                <span class="red">${{ slotProps.data.salePrice }}</span>
                <span class="strike">${{ slotProps.data.originalPrice }}</span>
              </div>
            </div>
          </div>
        </template>
      </Carousel>
    </div>
  </div>
</template>

<script>
import Carousel from "primevue/carousel";

const products = [
  {
    img: "https://slimages.macysassets.com/is/image/MCY/products/3/optimized/19621293_fpx.tif?bgc=255,255,255&wid=400&qlt=90,0&layer=comp&op_sharpen=0&resMode=bicub&op_usm=0.7,1.0,0.5,0&fmt=webp",
    brand: "Style & Co",
    name: "Solid Ribbed Muffler Scarf, Created for Macy's",
    salePrice: "12.99",
    originalPrice: "28.00",
  },
  {
    img: "https://slimages.macysassets.com/is/image/MCY/products/6/optimized/19783246_fpx.tif?bgc=255,255,255&wid=400&qlt=90,0&layer=comp&op_sharpen=0&resMode=bicub&op_usm=0.7,1.0,0.5,0&fmt=webp",
    brand: "Steve Madden",
    name: "Plaid Fringe-Trim Scarf",
    salePrice: "19.99",
    originalPrice: "42.00",
  },
  {
    img: "https://slimages.macysassets.com/is/image/MCY/products/9/optimized/15130629_fpx.tif?bgc=255,255,255&wid=400&qlt=90,0&layer=comp&op_sharpen=0&resMode=bicub&op_usm=0.7,1.0,0.5,0&fmt=webp",
    brand: "Glitzhome",
    name: "Plaid Scarf with Tassels",
    salePrice: "16.00",
    originalPrice: "",
  },
  {
    img: "https://slimages.macysassets.com/is/image/MCY/products/2/optimized/19643962_fpx.tif?bgc=255,255,255&wid=400&qlt=90,0&layer=comp&op_sharpen=0&resMode=bicub&op_usm=0.7,1.0,0.5,0&fmt=webp",
    brand: "Jenni",
    name: "On Repeat Jersey Wrap Scarf, Created for Macy's",
    salePrice: "19.99",
    originalPrice: "29.00",
  },
  {
    img: "https://slimages.macysassets.com/is/image/MCY/products/9/optimized/14662549_fpx.tif?bgc=255,255,255&wid=400&qlt=90,0&layer=comp&op_sharpen=0&resMode=bicub&op_usm=0.7,1.0,0.5,0&fmt=webp",
    brand: "V. Fraas",
    name: "Eco-Exploded Plaid Wrap Cashmink Scarf",
    salePrice: "40.95",
    originalPrice: "58.80",
  },
  {
    img: "https://slimages.macysassets.com/is/image/MCY/products/3/optimized/19621823_fpx.tif?bgc=255,255,255&wid=400&qlt=90,0&layer=comp&op_sharpen=0&resMode=bicub&op_usm=0.7,1.0,0.5,0&fmt=webp",
    brand: "Style & Co",
    name: "Space-Dye Ribbed Beanie, Created for Macy's",
    salePrice: "9.99",
    originalPrice: "20.00",
  },
];

export default {
  components: {
    Carousel,
  },
  setup() {
    return { products };
  },
};
</script>

<style scoped lang="scss">
.product-content {
  display: flex;
  letter-spacing: 0.1px;
  padding: 0.5rem;
  .link-btn {
    text-decoration: underline;
    font-size: 12px;
    cursor: pointer;
  }
  .red {
    color: #e01a2b;
  }
  .strike {
    text-decoration: line-through;
    margin: 0 0.5rem;
  }
  .bold {
    font-weight: bold;
  }
  .margin-b {
    margin-bottom: 1.5rem;
  }
  p {
    font-size: 14px;
    margin: 1.5rem 0;
  }
}
.product {
  display: flex;
  flex: 1;
  justify-content: space-between;
}
.imgs {
  width: 50%;
  img {
    max-width: 100%;
  }
}
.detail {
  width: 41%;
  .reverse-link {
    font-size: 14px;
    line-height: 1.28571;
    letter-spacing: 0.2px;
  }
  .product-title {
    font-size: 24px;
    font-weight: 300;
    line-height: 1.25;
  }
  .web-id {
    font-size: 12px;
    color: #626369;
    margin-bottom: 1rem;
    line-height: 1.5;
  }
  .stars {
    margin-bottom: 1.25rem;
    .grey-star {
      color: #959499;
    }
  }
  .legal {
    font-size: 12px;
    margin-bottom: 0.5rem;
  }
  .price {
    margin-bottom: 1.5rem;
    font-size: 18px;
  }
  .color-wrap {
    margin: 1.5rem 0;
    font-size: 14px;
  }
  .add-btn {
    display: block;
    border: none;
    height: 44px;
    width: 100%;
    background: #e01a2b;
    color: #fff;
    font-size: 16px;
    font-weight: 700;
    cursor: pointer;
    transition: all 0.25s;
    margin-bottom: 1rem;
    &:hover {
      background: #ab0000;
    }
  }
}
.carousel {
  width: 8rem;
  margin-left: 2.625rem;
  :deep(.p-carousel-content) .p-carousel-indicators {
    display: none;
  }
  .product-item {
    height: 260px;
    font-size: 14px;
    img {
      max-width: 100%;
      margin-bottom: 0.375rem;
    }
    a {
      color: #000;
      text-decoration: none;
      &:hover {
        text-decoration: underline;
      }
    }
    .product-name {
      overflow: hidden;
      text-overflow: ellipsis;
      display: -webkit-box;
      -webkit-line-clamp: 2;
      -webkit-box-orient: vertical;
    }
    .price {
      padding-top: 0.375rem;
    }
  }
}
</style>
