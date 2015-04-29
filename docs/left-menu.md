---
layout: page
title: Left Menu
---

##Layout

{% example html %}
<div style='height:500px;'>
	<div class='mc-leftmenu'>
		<div class='mc-leftmenu-logo'></div>
		<div class='mc-leftmenu-section'>
			<ul>
				<a class="active" href="#">
					<span class='active-ind'></span>
					<li><strong>Inbox</strong></li>
				</a>
				<a href="#"><li>Follow up</li></a>
				<a href="#"><li>Done</li></a>
			</ul>
		</div>
		<div class='mc-leftmenu-section'>
			<span class='mc-leftmenu-section-title'>
				<span class='glyphicon glyphicon-triangle-bottom'></span>
				LABELS
			</span>
			<ul>
				<a href="#"><li><span class="mc-leftmenu-item-label"></span>Team</li></a>
				<a href="#"><li><span class="mc-leftmenu-item-label"></span>Feedback</li></a>
			</ul>
		</div>
		<div class='mc-leftmenu-section'>
			<span class='mc-leftmenu-section-title'>
				<span class='glyphicon glyphicon-triangle-bottom'></span>
				OTHERS
			</span>
			<ul>
				<a href="#"><li>Spam</li></a>
				<a href="#"><li>Trash</li></a>
			</ul>
		</div>
	</div>
</div>
{% endexample %}