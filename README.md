<h1>Simple Code for integrating TinyMCE with Responsive Filemanager </h1> \ 
You can use this code into codeigniter as well \ 
local server must be installed in your system. i used xampp \

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


            <script type="text/javascript">
                var BASE_URL = "http://localhost/git/Integrate-TinyMCE-with-Responsive-Filemanager/"; // use your own base url
                tinymce.init({
                    selector: "#BlogDetails",
                    theme: "modern",
                    // width: 680,
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
                    external_filemanager_path: BASE_URL + "./filemanager/",
                    filemanager_title: "Media Gallery",
                    external_plugins: { "filemanager": BASE_URL + "./filemanager/plugin.min.js" }
                });
            </script>



4. Edit config.php file located at  filemanager/config folder.
5. Change the url of source and thumbs folder where files will be uploaded. 	
6. In config.php file you can also control file_number_limit_js, MaxSizeUpload, image_resizing and many more


Output : 

![alt text](./images/TinyMCE_default.png)
![alt text](./images/TinyMCE_filemanager.png)

 Find me on Facebook  : [ My Facebook profile link](https://www.facebook.com/morshed.riyad) \
 Find me on  Linkedin  : [My Linkedin profile  link](https://www.linkedin.com/in/monjur-morshed-riyadh-6aaba465/)