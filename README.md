# drupal_jammer
used inconjunction with google analytics to diable referrer spam
<pre>
  <?php if (function_exists('skivers_jammer_get_refer')): ?>
        <?php if (skivers_jammer_get_refer()): ?>
            <script>
                (function (i, s, o, g, r, a, m) {
                    i['GoogleAnalyticsObject'] = r;
                    i[r] = i[r] || function () {
                            (i[r].q = i[r].q || []).push(arguments)
                        }, i[r].l = 1 * new Date();
                    a = s.createElement(o),
                        m = s.getElementsByTagName(o)[0];
                    a.async = 1;
                    a.src = g;
                    m.parentNode.insertBefore(a, m)
                })(window, document, 'script', '//www.google-analytics.com/analytics.js', 'ga');

                ga('create', '[REPLACE ME WITH GOOGLE ANALYTICAL CODE]', 'auto');
                ga('send', 'pageview');
            </script>
        <?php endif; ?>
  <?php endif; ?>
</pre>