<template>
    <div>
        <Heador/>
        <Slider/>
        <Novice/>
        <Borrow/>
        <Money/>
        <Product/>
        <Life/>
        <Footor/>
        <Navbar/>
    </div>
</template>

<script>
import Heador from "../public/header"
import Footor from "../public/footer"
import Navbar from "../public/navbar"
import Slider from "./hslider"
import Novice from "./novice"
import Borrow from "./borrow"
import Money from "./money"
import Product from "./product"
import Life from "./life"

export default {
    components: {
        Heador,
        Slider,
        Novice,
        Borrow,
        Money,
        Product,
        Life,
        Footor,
        Navbar,
    },
}
</script>