# parcelviewergateway
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1">


    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.1/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-+0n0xVW2eSR5OomGNYDnhzAbDsOXxcvSN1TPprVMTNDbiYZCxYbOOl7+AMvyTG2x" crossorigin="anonymous">
    <link rel="preconnect" href="https://fonts.gstatic.com">
    <link href="https://fonts.googleapis.com/css2?family=Nanum+Gothic&display=swap" rel="stylesheet">

</head>

<style>
    body {
        font-family: 'Nanum Gothic', sans-serif;
        color: #2e2e2e;
        font-size: 16px;
    }

    .property-link {
        border-color: #61725f;
        background-color: #61725f;
        color: #e6ddb7;
        border-radius: 0;
        font-size: 16px;
    }

    .property-link:hover,
    .property-link:active,
    .property-link:focus,
    .property-link:target {
        border-color: #495648;
        background-color: #495648;
        color: #e6ddb7;
        border-radius: 0;
        font-size: 16px;
    }

    .form-control {
        border-radius: 0;
        font-size: 16px;
    }

</style>

<body>
    <div class="container-fluid">
        <form>
            <div class="row mb-3" style="padding-right:0; padding-top:30px">

                <div class="col-sm-12">
                    <input class="form-control" id="parcelInput" placeholder="Enter Property ID/UPI">
                </div>
            </div>
            <p style="text-align:right;margin-right:0">
                <a href="#" id="buttonLink" target="_blank" style="margin-right:8px"><button type="button" onclick="getInputValue()" formaction="#" class="btn btn-primary property-link">Map Parcel</button></a>
                <a href="#" id="detailsLink" target="_blank"><button type="button" onclick="getInputValue()" formaction="#" class="btn btn-primary property-link">Parcel Details</button></a>
            </p>
        </form>
    </div>


    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.0.1/dist/js/bootstrap.bundle.min.js" integrity="sha384-gtEjrD/SeCtmISkJkNUaaKMoLD0//ElJ19smozuHV6z3Iehds+3Ulb9Bn9Plx0x4" crossorigin="anonymous"></script>


    <script type="text/javascript">
        function getInputValue() {
            // Selecting the input element and get its value 
            var inputVal = document.getElementById("parcelInput").value;

            var parcelViewer = "https://gis.co.berks.pa.us/parcelviewer/index.html?find="

            var propertyDetails = "https://gis.co.berks.pa.us/ParcelSearch/Details.aspx?PropID="

            document.getElementById("buttonLink").href = parcelViewer + inputVal;
            document.getElementById("detailsLink").href = propertyDetails + inputVal;

        }

    </script>
</body>

</html>
