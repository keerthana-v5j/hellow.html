<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
  <!-- <link rel="stylesheet" href="E:\python\bootstrap\css\bootstrap.min.css"> -->
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/css/bootstrap.min.css" rel="stylesheet"
    integrity="sha384-EVSTQN3/azprG1Anm3QDgpJLIm9Nao0Yz1ztcQTwFspd3yD65VohhpuuCOmLASjC" crossorigin="anonymous">

  <style>
    .note {
      text-align: center;
      height: 80px;
      background: -webkit-linear-gradient(left, #0072ff, #8811c5);
      color: #fff;
      font-weight: bold;
      line-height: 80px;
    }

    body {
      margin: 0;
      font-family: 'Lato', sans-serif;
      font-size: 12px;
      line-height: 1.8em;
      text-transform: none;
      letter-spacing: .075em;
      font-weight: bold;
      font-style: normal;
      text-decoration: none;
      color: #e7bd74;
      background-color: rgb(17, 16, 17);
      display: block;
    }

    .title {
      margin-top: 2rem;
      margin-bottom: 1rem;
    }

    .form-content {
      padding: 5%;
      border: 1px solid #ced4da;
      margin-bottom: 2%;
    }

    .form-control {
      border-radius: 1.5rem;
    }

    .btnSubmit {
      border: none;
      border-radius: 1.5rem;
      padding: 1%;
      width: 20%;
      cursor: pointer;
      background: #0062cc;
      color: #fff;
    }

    h1 {
      font-family: sans-serif;
      display: block;
      font-size: 1rem;
      font-weight: bold;
      text-align: center;
      letter-spacing: 3px;
      color: hotpink;
      text-transform: uppercase;
      padding-top: 20px;
    }

    a {
      text-decoration: none;
      color: #fff;
    }

    a:hover {
      text-decoration: none;
      color: #fff;
    }
  </style>
</head>

<body>
  <!-- <script src="E:\python\bootstrap\js\bootstrap.min.js"></script> -->
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/js/bootstrap.bundle.min.js"
    integrity="sha384-MrcW6ZMFYlzcLA8Nl+NtUVF0sA7MsXsP1UyJoMp4YLEuNSfAP+JcXn/tWtIaxVXM"
    crossorigin="anonymous"></script>
  <script src="form.js"> </script>
  <script src="https://ajax.googleapis.com/ajax/libs/jquery/2.1.1/jquery.min.js"></script>
  <link rel="stylesheet" href="//code.jquery.com/ui/1.12.1/themes/base/jquery-ui.css">
  <script src="https://code.jquery.com/jquery-1.12.4.js"></script>
  <script src="https://code.jquery.com/ui/1.12.1/jquery-ui.js"></script>

  <div class="container register-form">
    <form class="requires-validation" novalidate>
    <div class="form">
      <div class="note">
        <h1> Bootstrap 4 Registration Form Example. </h1>
      </div>
      <div class="form-content" >
        <div class="row">
          <div class="col-md-4">
            <div class="form-group">
              <input type="text" class="form-control" id="username" placeholder="Your Name *" onkeypress="return (event.charCode > 64 && 
                              event.charCode < 91) || (event.charCode > 96 && event.charCode < 123)" required>
              <div class="valid-feedback">Looks good!</div>
              <div class="invalid-feedback">Please enter a name</div>

            </div>
            <script>
              (function () {
                'use strict'
                const forms = document.querySelectorAll('.requires-validation')
                Array.from(forms)
                  .forEach(function (form) {
                    form.addEventListener('submit', function (event) {
                      if (!form.checkValidity()) {
                        event.preventDefault()
                        event.stopPropagation()
                      }

                      form.classList.add('was-validated')
                    }, false)
                  })
              })()
            </script>
            <script> function isNumberKey(evt) {
                var charCode = (evt.which) ? evt.which : evt.keyCode
                if (charCode > 31 && (charCode < 48 || charCode > 57))
                  return false;
                return true;
              }
            </script>
            <div class="form-group">
              <input type="number" class="form-control" placeholder="Phone Number *" value=""
                onkeypress="return isNumberKey(event)" />
            </div>
          </div>

          <div class="col-md-6">
            <div class="form-group">
              <input type="text" class="form-control" placeholder="Your Password *" value="" />
            </div>
            <div class="form-group">
              <input type="text" class="form-control" placeholder="Confirm Password *" value="" />
            </div>
            <div class="form-group">
              <input class="form-control" placeholder="Enter DOB*" type="date" min="1999-01-1" max="2023-06-30" />
              <!-- <input type="date" name="party" min="2017-04-01" max="2017-04-30" /> -->

            </div>
          </div>
        </div>
        <div class="row align-items-center mt-4">
          <div class="col">
            <input type="text" class="form-control" placeholder=" Enter Email Address" onclick="validateEmail(this);" />
          </div>
          <div class="row align-items-center mt-4">
            <div class="col">
              <input type="text" class="form-control" placeholder=" Address">
            </div>
          </div>
          <div class="row justify-content-start mt-4">
            <div class="col">
              <div class="form-check">
                <label class="form-check-label">
                  <input type="checkbox" class="form-check-input">
                  I hereby agree to the <a href="/"> Terms and Conditions. </a>
                </label>
              </div>
              <button type="button" class="btnSubmit"> Submit </button>
            </div>
          </div>
        </div>
      </form>

</body>

</html>
