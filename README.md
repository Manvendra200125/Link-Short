1. Access the Website:
Go to "https://msn.ga/" in your web browser .

2. Shorten a URL:
On the webpage, enter a long URL (web address) that you want to make shorter.
Click the "Shorten URL" button.

3. Get Shortened URL:
A shortened URL like "https://msn.ga/XXXX" will be generated, where "XXXX" is a unique code.
This URL will appear on the page.

4. Copy and Share:
Copy the shortened URL.
Share this shortened URL with others through messages, emails, or social media.

5. Redirection:
When someone clicks the shortened URL, they'll be instantly redirected to the original long URL.

6. Benefits:
Simplifies long and complex URLs.

Convenient for sharing on platforms with character limits.
Provides a smoother user experience when accessing links.

![msn](https://github.com/Manvendra200125/Link-Short/assets/97372903/dfa972aa-6b8a-4dd5-b66a-ad39833fc7f7)

Logo of website 
![mm](https://github.com/Manvendra200125/Link-Short/assets/97372903/0d48ea73-d4ae-4b29-9b99-4dd9ae4cc78d)



<?php

function random_strings($length_of_string)
{
    // String of all alphanumeric characters
    $str_result = '0123456789abcdefghijklmnopqrstuvwxyz';

    // Shuffle the $str_result and return a substring of the specified length
    return substr(str_shuffle($str_result), 0, $length_of_string);
}

$a = 0;

if (isset($_POST['url'])) {
    $url = filter_var($_POST['url'], FILTER_SANITIZE_URL);

    // Validate the URL
    if (filter_var($url, FILTER_VALIDATE_URL) !== false) {
        $a = 1;
    } else {
        echo "<script>alert('Invalid URL')</script>";
    }

    $dir = random_strings(4);

    if (!is_dir($dir)) {
        mkdir($dir);
    } else {
        echo "<script>alert('Try Again!!')</script>";
    }

    $file = fopen($dir . '/index.html', "w");
    $txt = "
    <!DOCTYPE html>
    <html>
    <head>
        <meta charset='utf-8'>
        <title></title>
    </head>
    <body>
    </body>
    <script type='text/javascript'>window.location.href = '" . $url . "'</script>
    </html>
    ";
    fwrite($file, $txt);
    fclose($file);
}
?>

<!DOCTYPE html>
<html>
<head>
    <script async src="https://www.googletagmanager.com/gtag/js?id=G-28C8YCC8BR"></script>
    <script>
        window.dataLayer = window.dataLayer || [];
        function gtag() { dataLayer.push(arguments); }
        gtag('js', new Date());

        gtag('config', 'G-28C8YCC8BR');
    </script>
    <title>MSN</title>
</head>
<div class="center-image">
  <img src="mm.png" width="700" height="800" alt="Centered Image">
</div>
<style type="text/css">
  .center-image {
    display: flex;
    justify-content: center;
    width: 100%;
    height:0%;
    opacity: 0.2;
  }
    .form__group {
        position: relative;
        padding: 15px 0 0;
        margin-top: 10px;
        width: 80%;
    }

    .form__group1 {
        position: relative;
        padding: 15px 0 0;
        margin-top: 10px;
        width: 50%;
    }

    .form__field {
        font-family: inherit;
        width: 100%;
        border: 0;
        border-bottom: 2px solid #9b9b9b;
        outline: 0;
        font-size: 1.3rem;
        color: #e57373;
        padding: 7px 0;
        background: transparent;
        transition: border-color 0.2s;
    }

    .form__field::placeholder {
        color: transparent;
    }

    .form__field:placeholder-shown ~ .form__label {
        font-size: 1.3rem;
        cursor: text;
        top: 20px;
    }

    .form__label {
        position: absolute;
        top: 0;
        display: block;
        transition: 0.2s;
        font-size: 1rem;
        color: #9b9b9b;
    }

    .form__field:focus {
        padding-bottom: 6px;
        font-weight: bold;
        border-width: 3px;
        border-image: linear-gradient(to right, #11998e, #38ef7d);
        border-image-slice: 1;
    }

    .form__field:focus ~ .form__label {
        position: absolute;
        top: 0;
        display: block;
        transition: 0.2s;
        font-size: 1rem;
        color: #11998e;
        font-weight: 700;
    }

    .form__field:required,
    .form__field:out-of-range {
        border-color: #e57373;
    }

    .form__field:required ~ .form__label,
    .form__field:out-of-range ~ .form__label {
        color: #e57373;
    }

    

    .result {
        padding: 10px;
        margin-top: 20px;
        background-color: black;
        border-radius: 5px;
    }

    .result h2{
      color:#e57373;
    }

    .result a {
        color: #11998e;
        text-decoration: none;
        word-break: break-all;
        font-size: 40px;
    }
    
    html, body {
  height: 100%;
}

.wrap {
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
}

.button {
  min-width: 300px;
  min-height: 60px;
  font-family: 'Nunito', sans-serif;
  font-size: 22px;
  text-transform: uppercase;
  letter-spacing: 1.3px;
  font-weight: 700;
  color: #313133;
  background: #4FD1C5;
background: linear-gradient(90deg, rgba(129,230,217,1) 0%, rgba(79,209,197,1) 100%);
  border: none;
  border-radius: 1000px;
  box-shadow: 12px 12px 24px rgba(79,209,197,.64);
  transition: all 0.3s ease-in-out 0s;
  cursor: pointer;
  outline: none;
  position: relative;
  padding: 10px;
  }

button::before {
content: '';
  border-radius: 1000px;
  min-width: calc(300px + 12px);
  min-height: calc(60px + 12px);
  border: 6px solid #00FFCB;
  box-shadow: 0 0 60px rgba(0,255,203,.64);
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  opacity: 0;
  transition: all .3s ease-in-out 0s;
}

.button:hover, .button:focus {
  color: #313133;
  transform: translateY(-6px);
}

button:hover::before, button:focus::before {
  opacity: 1;
}

button::after {
  content: '';
  width: 30px; height: 30px;
  border-radius: 100%;
  border: 6px solid #00FFCB;
  position: absolute;
  z-index: -1;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  animation: ring 1.5s infinite;
}

button:hover::after, button:focus::after {
  animation: none;
  display: none;
}

@keyframes ring {
  0% {
    width: 30px;
    height: 30px;
    opacity: 1;
  }
  100% {
    width: 300px;
    height: 300px;
    opacity: 0;
  }
}


</style>
<a href="https://manvendra.my.canva.site/e-card" style="color: #11998e;">
  <img src=mm.png alt="Logo" style="width: 50px; height: 50px; margin-right: 5px;">
</a>
<body style="background-color:black;">
    <div style="text-align:center">
        <h1 style="color: #11998e;">MSN</h1>
        <h2 style="color: #11998e;">msn.ga is Short URL Maker</h2>
        

    </div>
    <form method="POST" action="" style="display: flex; justify-content: center;">
        <div class="form__group">
            <input type="url" class="form__field" placeholder="Enter URL" name="url" required>
            <label for="url" class="form__label">Enter URL</label><br><br>
        <div class="wrap">
                     <button class="button">Short URL</button>
        </div> 
        </div> 
    </form>

    <?php if ($a == 1) : ?>
        <div class="result" style="text-align: center;">
            <h2>Your Short URL:</h2>
            <a href="https://msn.ga/<?php echo $dir; ?>">https://msn.ga/<?php echo $dir; ?></a>
        </div>
    <?php endif; ?>
</body>
<style>
  @import url('https://fonts.googleapis.com/css?family=Montserrat:600&display=swap');
span{
  position: relative;
  display: inline-flex;
  width: 180px;
  height: 55px;
  margin: 0 15px;
  perspective: 1000px;
}
span a{
  font-size: 19px;
  letter-spacing: 1px;
  transform-style: preserve-3d;
  transform: translateZ(-25px);
  transition: transform .25s;
  font-family: 'Montserrat', sans-serif;
  
}
span a:before,
span a:after{
  position: absolute;
  content: "COPY URL";
  height: 55px;
  width: 180px;
  display: flex;
  align-items: center;
  justify-content: center;
  border: 5px solid #e57373;
  box-sizing: border-box;
  border-radius: 5px;
}
span a:before{
  color: #fff;
  background: #00FFCB;
  transform: rotateY(0deg) translateZ(25px);
}
span a:after{
  color: #00FFCB;
  transform: rotateX(90deg) translateZ(25px);
}
span a:hover{
  transform: translateZ(-25px) rotateX(-90deg);
}


</style>

		
<input type="url" class="form__field" placeholder="SUrl" value="<?php if ($a == 0){echo "";} else{echo 'https://msn.ga/'.$dir;} ?>" name="Surl" id='Surl' required /><br><br>
<span style="align:center;"><a href="javascript:copy()"></a></span>
	
<script>
function copy(){
  var copyText = document.getElementById("Surl");
  copyText.select();
  copyText.setSelectionRange(0, 99999);
  navigator.clipboard.writeText(copyText.value);
}

</script>


</html>
