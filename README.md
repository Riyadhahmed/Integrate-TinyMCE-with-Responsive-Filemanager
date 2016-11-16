<h1>Simple Code for integrating TinyMCE with Responsive Filemanager into a web page</h1>
you can use this code into codeigniter as well

To integrate TinyMCE with Responsive Filemanager we can follow some steps


Download this projects to view demo

Steps 

1. Copy and paste tinymce folder and filemanager folder into your root folder
2. In your web page where you view the TinyMCE editor add a textarea field like below code

            <div class = "col-md-10 form-group">
                <label for = "BlogDetails"> Blog Details </label>
                <textarea id = "BlogDetails" name = "blog_details" placeholder = "Write Here"></textarea>
            </div>
3. Add below script code into your web page


            <script type = "text/javascript">

                var BASE_URL = "http://localhost/Democode/TinyMCE_Responsive_Filemanager/";   // use your own base url


                tinymce.init({
                    selector: "#BlogDetails",   // your textarea id
                    theme: "modern",
                    // width: 680,    // you can add width and height as well
                    height: 200,
                    relative_urls: false,
                    remove_script_host: false,
                    // document_base_url: BASE_URL,
                    plugins: [
                        "advlist autolink link image lists charmap print preview hr anchor pagebreak",
                        "searchreplace wordcount visualblocks visualchars insertdatetime media nonbreaking",
                        "table contextmenu directionality emoticons paste textcolor responsivefilemanager code"
                    ],
                    toolbar1: "undo redo | bold italic underline | alignleft aligncenter alignright alignjustify | bullist numlist outdent indent | styleselect",
                    toolbar2: "| responsivefilemanager | link unlink anchor | image media | forecolor backcolor  | print preview code ",
                    image_advtab: true,

                    external_filemanager_path: BASE_URL + "filemanager/",      // filemanager folder
                    filemanager_title: "Media Gallery",
                    external_plugins: {"filemanager": BASE_URL + "filemanager/plugin.min.js"}   // plugin js file into your filemanger folder
                });
            </script>



4. Edit config.php file located at  filemanager/config folder.
5. Change the url of source and thumbs folder where files will be uploaded. 	
6. In config.php file you can also control file_number_limit_js, MaxSizeUpload, image_resizing and many more
