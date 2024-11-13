.. qnum::
   :prefix: exp-4-
   :start: 1

Practice Problems
============================


.. raw:: html

    <h3>loading...</h3>

    <script type="text/javascript">

      /*
      function getCookie(cname) {
         let name = cname + "=";
         let decodedCookie = decodeURIComponent(document.cookie);
         let ca = decodedCookie.split(';');
         for(let i = 0; i <ca.length; i++) {
            let c = ca[i];
            while (c.charAt(0) == ' ') {
               c = c.substring(1);
            }
            if (c.indexOf(name) == 0) {
               return c.substring(name.length, c.length);
            }
         }
         return "";
      }

      function setCookie(cname, cvalue) {
         document.cookie = cname + "=" + cvalue + ";";
      }*/

      window.onload = function() {

         //a = document.getElementById("hparsons_lg_sql_practice")
         var href = '';
         // get prev set cookie
         //var EXP_COOKIE = 'hparsons_lg_sql_221115'
         //var cond = getCookie(EXP_COOKIE);
         // not using cookie here; random assignment
         var cond = '';
         // if no prev set cookie: generate random condition and set cookie
         if (cond != 'wr' && cond != 'hp') {
            var v = Math.floor(Math.random() * 2);
            if (v < 1) {
                cond = 'wr';
            } else {
                cond = 'hp';
            }
            //setCookie(EXP_COOKIE, cond);
         }

         if (cond == 'wr') {
            href = "topic-3-13-experiment-practice-W.html"
         } else if (cond == 'hp') {
            href = "topic-3-13-experiment-practice-P.html"
         }
         window.location.href = href;
      };
    </script>