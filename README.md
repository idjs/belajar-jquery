belajar-jquery
==============

Dasar dan Penggunaan JQuery
---------------------------
Maintained by Henyana

#Daftar Isi:#
1. Apa itu jQuery?
2. Siapa yang menggunakan jQuery
3. DOM Traversal and Manipulation
4. Event Handling
5. Ajax

#1. Apa itu jQuery?#
jQuery adalah sebuah library berbahasa pemrograman JavaScript yang cepat, dengan ukuran file yang relatif kecil dan kaya akan fitur. jQuery dapat membuat hal-hal seperti traversal dan manipulasi dokumen HTML, penanganan event, animasi dan penggunaan Ajax yang jauh lebih sederhana dengan kemudahan menggunakan API yang bekerja di banyak browser. Dengan kombinasi fleksibilitas dan ekstenbilitas, jQuery telah mengubah cara jutaan orang menulis JavaScript.

#2. Siapa yang menggunakan jQuery#

#3. DOM Traversal and Manipulation#
Ambil element `<button>` yang memiliki class 'continue' dan ubah HTML-nya menjadi 'Next Step...'

`$('button.continue').html('Next Step...');`

#4. Event Handling#
Munculkan element #banner-message yang sedang dalam keaadaan hidden dengan in-line CSS `display:none` ketika button element `#button-container' menerima event klik.

`var hiddenBox = $('#banner-message');`
`$('#button-container button').on('click', function (event) {`
`	hiddenBox.show();`
`});`

#5. Ajax#
Memanggil script local pada server `/api/getWeather` dengan parameter query `zipcode=97201` kemudian replace element `#weather-temp` dengan text hasil.

`$.ajax({`
`  url: '/api/getWeather',`
`  data: {`
`    zipcode: 97201`
`  },`
`  success: function( data ) {`
`    $('#weather-temp').html('<strong>' + data + '</strong> degrees');`
`  }`
`});`