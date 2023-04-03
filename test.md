<html>
<script src="https://ajax.googleapis.com/ajax/libs/jquery/2.1.1/jquery.min.js"></script>

<img src="https://upload.wikimedia.org/wikipedia/commons/7/77/Avatar_cat.png" height="256" width="256" alt="kitten" id="imageid">

  <script>
    document.getElementById("imageid").addEventListener('click', function (event) {
      bounds=this.getBoundingClientRect();
      var left=bounds.left;
      var top=bounds.top;
      var x = event.pageX - left;
      var y = event.pageY - top;
      var cw=this.clientWidth
      var ch=this.clientHeight
      var iw=this.naturalWidth
      var ih=this.naturalHeight
      var px=x/cw*iw
      var py=y/ch*ih
      alert("mouse pos ("+x+", " + y+ ") | client image size: "+cw+" x "+ch+" | natural image size: "+iw+" x "+ih );
    });
  </script>

</html>