
🏝️🏖️💯 Introduce your customers to your app before they start using your app

`onboard.css` is a multistep onboarding screen, you can use it to introduce your customers to your app, or collect additional information from them before they start using your app.

## Installation

Install via npm:

```bash
$ npm install onboard.css
```

## Usage
onboard.css work with bootstrap and Slick carroussel so if you want to use onboard.css in your website , you have to put these following items in your `<head>` and before your `</body>`

```html
<head>
  <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/slick-carousel/1.9.0/slick.min.css">
  <link rel="stylesheet" href="osfont-icon.css"> <!-- Osfont icon is used to display slick icons -->
  <link rel="stylesheet" href="onboard.min.css">
</head>
<body>
    Your content here

    <script src="https://code.jquery.com/jquery-3.4.1.min.js"></script>
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/js/bootstrap.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/slick-carousel/1.9.0/slick.min.js"></script>
</body>
```

or use a Github hosted version

```html
<head>
  <link rel="stylesheet" href="https://raw.githubusercontent.com/andreatchori/onboard.css/master/sources/onboard.min.css">
</head>
```


### Shape

| Class Name        |                    |                     |                      |
| ----------------- | ------------------ | ------------------- | -------------------- |
| `straight-line`   | `slice-left`       | `slice-right`       | `curve-left`         |
| `curve-right`     | 

### Title

| Class Name        |                    |                     |                      |
| ----------------- | ------------------ | ------------------- | -------------------- |
| `title-blue`      | `title-purple`     | `title-pink`        | `title-red`          |
| `title-indigo`    |`title-orange`      | `title-yellow`      | `title-green`        |
| `title-teal`      |`title-cyan`        | `title-gray-dark`   | `title-danger`       |
| `title-primary`   |`title-success`     | `title-info`        | `title-warning`      |
| `title-light`     |`title-dark`        | 

### Background

| Class Name        |                    |                     |                      |
| ----------------- | ------------------ | ------------------- | -------------------- |
| `background-blue` | `background-purple`| `background-pink`   | `background-red`     |
| `background-indigo`|`background-orange`| `background-yellow` | `background-green`   |
| `background-teal`|`background-cyan`    | `background-gray-dark` | `background-danger` |


Full example:

```html
    <div class="onboard-modal modal fade animated show-on-load">
        <div class="modal-dialog modal-centered">
            <div class="modal-content text-center">
                <button aria-label="Close" class="close" data-dismiss="modal" type="button">
                    <span class="close-label">Skip Intro</span>
                    <span class="os-icon os-icon-close"></span>
                </button>
                <div class="onboard-slider-container">
                    <div class="onboard-slide">
                        <div class="onboard-media">
                            <img alt="" src="assets/img/your-images.png" width="120px">
                        </div>
                        <div class="content">
                            <h4 class="onboard-title">
                                Put your title here
                            </h4>
                            <div class="onboard-text">
                                Put your description here
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
```

### Launch modal on page load
Put this script before your `</body>`
```javascript
    $('.onboard-modal.show-on-load').modal('show');
        if ($('.onboard-modal .onboard-slider-container').length) {
            $('.onboard-modal .onboard-slider-container').slick({
                dots: true,
                infinite: false,
                adaptiveHeight: true,
                slidesToShow: 1,
                slidesToScroll: 1
            });
            $('.onboard-modal').on('shown.bs.modal', function (e) {
                $('.onboard-modal .onboard-slider-container').slick('setPosition');
            });
    }
```

## Contributing

Pull requests are the way to go here. We only have two rules for submitting a pull request: match the naming convention (camelCase) and let us see a demo of submitted animations in a [pen](http://codepen.io). That **last one is important**.
