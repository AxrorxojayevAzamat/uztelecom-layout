<section>
    <h1>Sotuv ofislari joylashuvi</h1>
    <div class="map" >

        <Map {options}/>

    </div>

</section>



<script>

    import Map from '@anoram/leaflet-svelte'

  
    let options = {
        scrollWheelZoom: false,
        center: [41.311081, 69.240562],

        markers: [

            {

                lat: 41.311081,

                lng: 69.340563

            }, {

                lat: 41.311081,

                lng: 69.240564

            }, {

                lat: 41.311081,

                lng: 69.249565

            }, {

                lat: 41.311881,

                lng: 69.24566

            }, {

                lat: 41.311881,

                lng: 69.24566

            }, {

                lat: 41.311881,

                lng: 69.24566

            }, {

                lat: 41.311881,

                lng: 69.24566

            },

        ],

        mapID: "map"

    }

</script>



<style type="text/scss">
h1
{
    font: 500 36px/48px Montserrat,sans-serif;
    color: #212f3d;
    text-align: center;
}
    div {

        padding-top: 50px;

    }



    .map {

        height: 600px;
        width: auto;

    }

</style>