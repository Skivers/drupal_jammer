# drupal_jammer
used inconjunction with google analytics to disable referrer spam

		<?php if (function_exists('skivers_jammer_get_refer')): ?>
        	<?php if (skivers_jammer_get_refer()): ?>
                <!-- javascript for google analytics -->
        	<?php endif; ?>
  		<?php endif; ?>
