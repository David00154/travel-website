<script>
    import axios from "axios"
    let name;
    let email;
    let phone;
    let address;
    let location;
    let guests;
    let arrivals;
    let leaving;
    function makeBookings() {
        // axios
        // .post('/book/makeBookings', {
        //      name,
        //      email,
        //      phone,
        //      address,
        //      location,
        //      guests,
        //      arrivals,
        //      leaving,
        // })
        // .then(({request}) => {
        //     if(request.status == 200) {
        //         alert("Travel booking made.")
        //         wipeFormData()
        //     }
        // })
        // .catch((e) => {
        //     // if(e) alert("Internal server error.")
        //     alert("Internal server error.")
        //     // console.log(e)
        // })
    }

    function wipeFormData() {
         name = ""
         email = ""
         phone = ""
         address = ""
         location = ""
         guests = ""
         arrivals = ""
         leaving = ""
    }
</script>


<div class="heading" style="background:url(/images/header-bg-3.png) no-repeat">
    <h1>book now</h1>
</div>

<!-- booking section starts  -->

<section class="booking">

    <h1 class="heading-title">book your trip!</h1>

    <form method="post" on:submit|preventDefault="{makeBookings}" class="book-form">

        <div class="flex">
            <div class="inputBox">
                <span>name :</span>
                <input type="text" bind:value="{name}" placeholder="enter your name" name="name">
            </div>
            <div class="inputBox">
                <span>email :</span>
                <input type="email" bind:value="{email}" placeholder="enter your email" name="email">
            </div>
            <div class="inputBox">
                <span>phone :</span>
                <input type="number" bind:value="{phone}" placeholder="enter your number" name="phone">
            </div>
            <div class="inputBox">
                <span>address :</span>
                <input type="text" bind:value="{address}" placeholder="enter your address" name="address">
            </div>
            <div class="inputBox">
                <span>where to :</span>
                <input type="text" bind:value="{location}" placeholder="place you want to visit" name="location">
            </div>
            <div class="inputBox">
                <span>how many :</span>
                <input type="number" bind:value="{guests}" placeholder="number of guests" name="guests">
            </div>
            <div class="inputBox">
                <span>arrivals :</span>
                <input type="date" bind:value="{arrivals}" name="arrivals">
            </div>
            <div class="inputBox">
                <span>leaving :</span>
                <input type="date" bind:value="{leaving}" name="leaving">
            </div>
        </div>

        <input type="submit" value="submit" class="btn" name="send">

    </form>

</section>

<!-- booking section ends -->
