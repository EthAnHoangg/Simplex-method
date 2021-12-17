<html><head><meta http-equiv="Content-Type" content="text/html; charset=utf-8"/><title>SIMPLEX METHOD</title><style>
/* cspell:disable-file */
/* webkit printing magic: print all background colors */
html {
	-webkit-print-color-adjust: exact;
}
* {
	box-sizing: border-box;
	-webkit-print-color-adjust: exact;
}

html,
body {
	margin: 0;
	padding: 0;
}
@media only screen {
	body {
		margin: 2em auto;
		max-width: 900px;
		color: rgb(55, 53, 47);
	}
}

body {
	line-height: 1.5;
	white-space: pre-wrap;
}

a,
a.visited {
	color: inherit;
	text-decoration: underline;
}

.pdf-relative-link-path {
	font-size: 80%;
	color: #444;
}

h1,
h2,
h3 {
	letter-spacing: -0.01em;
	line-height: 1.2;
	font-weight: 600;
	margin-bottom: 0;
}

.page-title {
	font-size: 2.5rem;
	font-weight: 700;
	margin-top: 0;
	margin-bottom: 0.75em;
}

h1 {
	font-size: 1.875rem;
	margin-top: 1.875rem;
}

h2 {
	font-size: 1.5rem;
	margin-top: 1.5rem;
}

h3 {
	font-size: 1.25rem;
	margin-top: 1.25rem;
}

.source {
	border: 1px solid #ddd;
	border-radius: 3px;
	padding: 1.5em;
	word-break: break-all;
}

.callout {
	border-radius: 3px;
	padding: 1rem;
}

figure {
	margin: 1.25em 0;
	page-break-inside: avoid;
}

figcaption {
	opacity: 0.5;
	font-size: 85%;
	margin-top: 0.5em;
}

mark {
	background-color: transparent;
}

.indented {
	padding-left: 1.5em;
}

hr {
	background: transparent;
	display: block;
	width: 100%;
	height: 1px;
	visibility: visible;
	border: none;
	border-bottom: 1px solid rgba(55, 53, 47, 0.09);
}

img {
	max-width: 100%;
}

@media only print {
	img {
		max-height: 100vh;
		object-fit: contain;
	}
}

@page {
	margin: 1in;
}

.collection-content {
	font-size: 0.875rem;
}

.column-list {
	display: flex;
	justify-content: space-between;
}

.column {
	padding: 0 1em;
}

.column:first-child {
	padding-left: 0;
}

.column:last-child {
	padding-right: 0;
}

.table_of_contents-item {
	display: block;
	font-size: 0.875rem;
	line-height: 1.3;
	padding: 0.125rem;
}

.table_of_contents-indent-1 {
	margin-left: 1.5rem;
}

.table_of_contents-indent-2 {
	margin-left: 3rem;
}

.table_of_contents-indent-3 {
	margin-left: 4.5rem;
}

.table_of_contents-link {
	text-decoration: none;
	opacity: 0.7;
	border-bottom: 1px solid rgba(55, 53, 47, 0.18);
}

table,
th,
td {
	border: 1px solid rgba(55, 53, 47, 0.09);
	border-collapse: collapse;
}

table {
	border-left: none;
	border-right: none;
}

th,
td {
	font-weight: normal;
	padding: 0.25em 0.5em;
	line-height: 1.5;
	min-height: 1.5em;
	text-align: left;
}

th {
	color: rgba(55, 53, 47, 0.6);
}

ol,
ul {
	margin: 0;
	margin-block-start: 0.6em;
	margin-block-end: 0.6em;
}

li > ol:first-child,
li > ul:first-child {
	margin-block-start: 0.6em;
}

ul > li {
	list-style: disc;
}

ul.to-do-list {
	text-indent: -1.7em;
}

ul.to-do-list > li {
	list-style: none;
}

.to-do-children-checked {
	text-decoration: line-through;
	opacity: 0.375;
}

ul.toggle > li {
	list-style: none;
}

ul {
	padding-inline-start: 1.7em;
}

ul > li {
	padding-left: 0.1em;
}

ol {
	padding-inline-start: 1.6em;
}

ol > li {
	padding-left: 0.2em;
}

.mono ol {
	padding-inline-start: 2em;
}

.mono ol > li {
	text-indent: -0.4em;
}

.toggle {
	padding-inline-start: 0em;
	list-style-type: none;
}

/* Indent toggle children */
.toggle > li > details {
	padding-left: 1.7em;
}

.toggle > li > details > summary {
	margin-left: -1.1em;
}

.selected-value {
	display: inline-block;
	padding: 0 0.5em;
	background: rgba(206, 205, 202, 0.5);
	border-radius: 3px;
	margin-right: 0.5em;
	margin-top: 0.3em;
	margin-bottom: 0.3em;
	white-space: nowrap;
}

.collection-title {
	display: inline-block;
	margin-right: 1em;
}

.simple-table {
	margin-top: 1em;
	font-size: 0.875rem;
}

.simple-table-header {
	background: rgb(247, 246, 243);
	color: black;
	font-weight: 500;
}

time {
	opacity: 0.5;
}

.icon {
	display: inline-block;
	max-width: 1.2em;
	max-height: 1.2em;
	text-decoration: none;
	vertical-align: text-bottom;
	margin-right: 0.5em;
}

img.icon {
	border-radius: 3px;
}

.user-icon {
	width: 1.5em;
	height: 1.5em;
	border-radius: 100%;
	margin-right: 0.5rem;
}

.user-icon-inner {
	font-size: 0.8em;
}

.text-icon {
	border: 1px solid #000;
	text-align: center;
}

.page-cover-image {
	display: block;
	object-fit: cover;
	width: 100%;
	max-height: 30vh;
}

.page-header-icon {
	font-size: 3rem;
	margin-bottom: 1rem;
}

.page-header-icon-with-cover {
	margin-top: -0.72em;
	margin-left: 0.07em;
}

.page-header-icon img {
	border-radius: 3px;
}

.link-to-page {
	margin: 1em 0;
	padding: 0;
	border: none;
	font-weight: 500;
}

p > .user {
	opacity: 0.5;
}

td > .user,
td > time {
	white-space: nowrap;
}

input[type="checkbox"] {
	transform: scale(1.5);
	margin-right: 0.6em;
	vertical-align: middle;
}

p {
	margin-top: 0.5em;
	margin-bottom: 0.5em;
}

.image {
	border: none;
	margin: 1.5em 0;
	padding: 0;
	border-radius: 0;
	text-align: center;
}

.code,
code {
	background: rgba(135, 131, 120, 0.15);
	border-radius: 3px;
	padding: 0.2em 0.4em;
	border-radius: 3px;
	font-size: 85%;
	tab-size: 2;
}

code {
	color: #eb5757;
}

.code {
	padding: 1.5em 1em;
}

.code-wrap {
	white-space: pre-wrap;
	word-break: break-all;
}

.code > code {
	background: none;
	padding: 0;
	font-size: 100%;
	color: inherit;
}

blockquote {
	font-size: 1.25em;
	margin: 1em 0;
	padding-left: 1em;
	border-left: 3px solid rgb(55, 53, 47);
}

.bookmark {
	text-decoration: none;
	max-height: 8em;
	padding: 0;
	display: flex;
	width: 100%;
	align-items: stretch;
}

.bookmark-title {
	font-size: 0.85em;
	overflow: hidden;
	text-overflow: ellipsis;
	height: 1.75em;
	white-space: nowrap;
}

.bookmark-text {
	display: flex;
	flex-direction: column;
}

.bookmark-info {
	flex: 4 1 180px;
	padding: 12px 14px 14px;
	display: flex;
	flex-direction: column;
	justify-content: space-between;
}

.bookmark-image {
	width: 33%;
	flex: 1 1 180px;
	display: block;
	position: relative;
	object-fit: cover;
	border-radius: 1px;
}

.bookmark-description {
	color: rgba(55, 53, 47, 0.6);
	font-size: 0.75em;
	overflow: hidden;
	max-height: 4.5em;
	word-break: break-word;
}

.bookmark-href {
	font-size: 0.75em;
	margin-top: 0.25em;
}

.sans { font-family: ui-sans-serif, -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, "Apple Color Emoji", Arial, sans-serif, "Segoe UI Emoji", "Segoe UI Symbol"; }
.code { font-family: "SFMono-Regular", Menlo, Consolas, "PT Mono", "Liberation Mono", Courier, monospace; }
.serif { font-family: Lyon-Text, Georgia, ui-serif, serif; }
.mono { font-family: iawriter-mono, Nitti, Menlo, Courier, monospace; }
.pdf .sans { font-family: Inter, ui-sans-serif, -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, "Apple Color Emoji", Arial, sans-serif, "Segoe UI Emoji", "Segoe UI Symbol", 'Twemoji', 'Noto Color Emoji', 'Noto Sans CJK JP'; }
.pdf:lang(zh-CN) .sans { font-family: Inter, ui-sans-serif, -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, "Apple Color Emoji", Arial, sans-serif, "Segoe UI Emoji", "Segoe UI Symbol", 'Twemoji', 'Noto Color Emoji', 'Noto Sans CJK SC'; }
.pdf:lang(zh-TW) .sans { font-family: Inter, ui-sans-serif, -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, "Apple Color Emoji", Arial, sans-serif, "Segoe UI Emoji", "Segoe UI Symbol", 'Twemoji', 'Noto Color Emoji', 'Noto Sans CJK TC'; }
.pdf:lang(ko-KR) .sans { font-family: Inter, ui-sans-serif, -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, "Apple Color Emoji", Arial, sans-serif, "Segoe UI Emoji", "Segoe UI Symbol", 'Twemoji', 'Noto Color Emoji', 'Noto Sans CJK KR'; }
.pdf .code { font-family: Source Code Pro, "SFMono-Regular", Menlo, Consolas, "PT Mono", "Liberation Mono", Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK JP'; }
.pdf:lang(zh-CN) .code { font-family: Source Code Pro, "SFMono-Regular", Menlo, Consolas, "PT Mono", "Liberation Mono", Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK SC'; }
.pdf:lang(zh-TW) .code { font-family: Source Code Pro, "SFMono-Regular", Menlo, Consolas, "PT Mono", "Liberation Mono", Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK TC'; }
.pdf:lang(ko-KR) .code { font-family: Source Code Pro, "SFMono-Regular", Menlo, Consolas, "PT Mono", "Liberation Mono", Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK KR'; }
.pdf .serif { font-family: PT Serif, Lyon-Text, Georgia, ui-serif, serif, 'Twemoji', 'Noto Color Emoji', 'Noto Serif CJK JP'; }
.pdf:lang(zh-CN) .serif { font-family: PT Serif, Lyon-Text, Georgia, ui-serif, serif, 'Twemoji', 'Noto Color Emoji', 'Noto Serif CJK SC'; }
.pdf:lang(zh-TW) .serif { font-family: PT Serif, Lyon-Text, Georgia, ui-serif, serif, 'Twemoji', 'Noto Color Emoji', 'Noto Serif CJK TC'; }
.pdf:lang(ko-KR) .serif { font-family: PT Serif, Lyon-Text, Georgia, ui-serif, serif, 'Twemoji', 'Noto Color Emoji', 'Noto Serif CJK KR'; }
.pdf .mono { font-family: PT Mono, iawriter-mono, Nitti, Menlo, Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK JP'; }
.pdf:lang(zh-CN) .mono { font-family: PT Mono, iawriter-mono, Nitti, Menlo, Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK SC'; }
.pdf:lang(zh-TW) .mono { font-family: PT Mono, iawriter-mono, Nitti, Menlo, Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK TC'; }
.pdf:lang(ko-KR) .mono { font-family: PT Mono, iawriter-mono, Nitti, Menlo, Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK KR'; }
.highlight-default {
	color: rgba(55, 53, 47, 1);
}
.highlight-gray {
	color: rgba(120, 119, 116, 1);
	fill: rgba(145, 145, 142, 1);
}
.highlight-brown {
	color: rgba(159, 107, 83, 1);
	fill: rgba(187, 132, 108, 1);
}
.highlight-orange {
	color: rgba(217, 115, 13, 1);
	fill: rgba(215, 129, 58, 1);
}
.highlight-yellow {
	color: rgba(203, 145, 47, 1);
	fill: rgba(203, 148, 51, 1);
}
.highlight-teal {
	color: rgba(68, 131, 97, 1);
	fill: rgba(108, 155, 125, 1);
}
.highlight-blue {
	color: rgba(51, 126, 169, 1);
	fill: rgba(91, 151, 189, 1);
}
.highlight-purple {
	color: rgba(144, 101, 176, 1);
	fill: rgba(167, 130, 195, 1);
}
.highlight-pink {
	color: rgba(193, 76, 138, 1);
	fill: rgba(205, 116, 159, 1);
}
.highlight-red {
	color: rgba(212, 76, 71, 1);
	fill: rgba(225, 111, 100, 1);
}
.highlight-gray_background {
	background: rgba(241, 241, 239, 1);
}
.highlight-brown_background {
	background: rgba(244, 238, 238, 1);
}
.highlight-orange_background {
	background: rgba(251, 236, 221, 1);
}
.highlight-yellow_background {
	background: rgba(251, 243, 219, 1);
}
.highlight-teal_background {
	background: rgba(237, 243, 236, 1);
}
.highlight-blue_background {
	background: rgba(231, 243, 248, 1);
}
.highlight-purple_background {
	background: rgba(244, 240, 247, 0.8);
}
.highlight-pink_background {
	background: rgba(249, 238, 243, 0.8);
}
.highlight-red_background {
	background: rgba(253, 235, 236, 1);
}
.block-color-default {
	color: inherit;
	fill: inherit;
}
.block-color-gray {
	color: rgba(120, 119, 116, 1);
	fill: rgba(145, 145, 142, 1);
}
.block-color-brown {
	color: rgba(159, 107, 83, 1);
	fill: rgba(187, 132, 108, 1);
}
.block-color-orange {
	color: rgba(217, 115, 13, 1);
	fill: rgba(215, 129, 58, 1);
}
.block-color-yellow {
	color: rgba(203, 145, 47, 1);
	fill: rgba(203, 148, 51, 1);
}
.block-color-teal {
	color: rgba(68, 131, 97, 1);
	fill: rgba(108, 155, 125, 1);
}
.block-color-blue {
	color: rgba(51, 126, 169, 1);
	fill: rgba(91, 151, 189, 1);
}
.block-color-purple {
	color: rgba(144, 101, 176, 1);
	fill: rgba(167, 130, 195, 1);
}
.block-color-pink {
	color: rgba(193, 76, 138, 1);
	fill: rgba(205, 116, 159, 1);
}
.block-color-red {
	color: rgba(212, 76, 71, 1);
	fill: rgba(225, 111, 100, 1);
}
.block-color-gray_background {
	background: rgba(241, 241, 239, 1);
}
.block-color-brown_background {
	background: rgba(244, 238, 238, 1);
}
.block-color-orange_background {
	background: rgba(251, 236, 221, 1);
}
.block-color-yellow_background {
	background: rgba(251, 243, 219, 1);
}
.block-color-teal_background {
	background: rgba(237, 243, 236, 1);
}
.block-color-blue_background {
	background: rgba(231, 243, 248, 1);
}
.block-color-purple_background {
	background: rgba(244, 240, 247, 0.8);
}
.block-color-pink_background {
	background: rgba(249, 238, 243, 0.8);
}
.block-color-red_background {
	background: rgba(253, 235, 236, 1);
}
.select-value-color-pink { background-color: rgba(245, 224, 233, 1); }
.select-value-color-purple { background-color: rgba(232, 222, 238, 1); }
.select-value-color-green { background-color: rgba(219, 237, 219, 1); }
.select-value-color-gray { background-color: rgba(227, 226, 224, 1); }
.select-value-color-orange { background-color: rgba(250, 222, 201, 1); }
.select-value-color-brown { background-color: rgba(238, 224, 218, 1); }
.select-value-color-red { background-color: rgba(255, 226, 221, 1); }
.select-value-color-yellow { background-color: rgba(253, 236, 200, 1); }
.select-value-color-blue { background-color: rgba(211, 229, 239, 1); }

.checkbox {
	display: inline-flex;
	vertical-align: text-bottom;
	width: 16;
	height: 16;
	background-size: 16px;
	margin-left: 2px;
	margin-right: 5px;
}

.checkbox-on {
	background-image: url("data:image/svg+xml;charset=UTF-8,%3Csvg%20width%3D%2216%22%20height%3D%2216%22%20viewBox%3D%220%200%2016%2016%22%20fill%3D%22none%22%20xmlns%3D%22http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%22%3E%0A%3Crect%20width%3D%2216%22%20height%3D%2216%22%20fill%3D%22%2358A9D7%22%2F%3E%0A%3Cpath%20d%3D%22M6.71429%2012.2852L14%204.9995L12.7143%203.71436L6.71429%209.71378L3.28571%206.2831L2%207.57092L6.71429%2012.2852Z%22%20fill%3D%22white%22%2F%3E%0A%3C%2Fsvg%3E");
}

.checkbox-off {
	background-image: url("data:image/svg+xml;charset=UTF-8,%3Csvg%20width%3D%2216%22%20height%3D%2216%22%20viewBox%3D%220%200%2016%2016%22%20fill%3D%22none%22%20xmlns%3D%22http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%22%3E%0A%3Crect%20x%3D%220.75%22%20y%3D%220.75%22%20width%3D%2214.5%22%20height%3D%2214.5%22%20fill%3D%22white%22%20stroke%3D%22%2336352F%22%20stroke-width%3D%221.5%22%2F%3E%0A%3C%2Fsvg%3E");
}
	
</style></head><body><article id="50a08aa1-d9ad-418f-8a65-8d6bd881777f" class="page sans"><header><h1 class="page-title">SIMPLEX METHOD</h1></header><div class="page-body"><p id="fdab90b7-6220-463e-be03-34a05d7ecea4" class=""><strong>(PHƯƠNG PHÁP ĐƠN HÌNH)</strong></p><p id="34b34ecd-0d40-4148-8e7c-8a9cdcb7b3b6" class="">Hoang An, based on <a href="http://math.libretexts.org/">math.libretexts.org</a></p><p id="2da84a44-3c3f-4f44-a200-2f97f25074e1" class="">Nghe An - 18:49 - Thursday, December 16, 2021</p><hr id="36a7a7cb-5dbf-44d5-9d41-1c07e4b9d013"/><h1 id="aa337d7b-0bf4-4923-8c1c-8838806894a3" class="">Introduction</h1><p id="6fa151bd-9e21-448c-ad93-d202bd22f929" class="">The simplex method uses an approach that is very efficient. It does not compute the value of the objective function at every point; instead, it begins with a corner point of the feasibility region where all the main variables are zero and then systematically moves from corner point to corner point, while improving the value of the objective function at each stage. The process continues until the optimal solution is found.</p><h1 id="fd7b8f8c-c355-4d0f-96d4-ea209e821419" class="">General Algorithm</h1><ol type="1" id="837688f9-21f3-42cb-b865-f5235705fb56" class="numbered-list" start="1"><li><strong>Set up the problem.
</strong>That is, write the objective function and the inequality constraints.</li></ol><ol type="1" id="88261252-5c43-48ef-8bc7-07cee2b358ff" class="numbered-list" start="2"><li><strong>Convert the inequalities into equations. 
</strong>This is done by adding one slack variable for each inequality.</li></ol><ol type="1" id="e5b362fd-b433-4337-8307-e0245c0bd5cc" class="numbered-list" start="3"><li><strong>Construct the initial simplex tableau. 
</strong>Write the objective function as the bottom row.</li></ol><ol type="1" id="3a04ad95-265d-47b9-b651-f9cd476bb0ea" class="numbered-list" start="4"><li><strong>The most negative entry in the bottom row identifies the pivot column.</strong></li></ol><ol type="1" id="ac23c673-a310-405e-80de-a31a54575936" class="numbered-list" start="5"><li><strong>Calculate the quotients. The smallest quotient identifies a row. The element in the intersection of the column identified in step 4 and the row identified in this step is identified as the pivot element. 
</strong>The quotients are computed by dividing the far right column by the identified column in step 4. A quotient that is a zero, or a negative number, or that has a zero in the denominator, is ignored.</li></ol><ol type="1" id="cf59fe24-5cd0-4179-929f-e981e123e0ed" class="numbered-list" start="6"><li><strong>Perform pivoting to make all other entries in this column zero. 
</strong>This is done the same way as we did with the Gauss-Jordan method.</li></ol><ol type="1" id="f5f904e7-16f7-4656-be4c-c721ece25b2e" class="numbered-list" start="7"><li><strong>When there are no more negative entries in the bottom row, we are finished; otherwise, we start again from step 4.</strong></li></ol><ol type="1" id="72290013-519b-4358-bac5-86ca42abed0a" class="numbered-list" start="8"><li><strong>Read off your answers. 
</strong>Get the variables using the columns with 1 and 0s. All other variables are zero. The maximum value you are looking for appears in the bottom right hand corner.</li></ol><hr id="0db53530-bcd6-423b-ba23-3a5b54f21070"/><h1 id="5cb5d15a-a85e-455d-81da-5ba0d78d5da5" class="">Example</h1><h3 id="e2e5cebd-241e-4ff3-a229-69a1e68c3375" class="">Example 1</h3><p id="5a5f2b09-c55b-4ef4-aa99-cd51437db6be" class="">Niki holds two part-time jobs, Job I and Job II. She never wants to work more than a total of 12 hours a week. She has determined that for every hour she works at Job I, she needs 2 hours of preparation time, and for every hour she works at Job II, she needs one hour of preparation time, and she cannot spend more than 16 hours for preparation. If she makes $40 an hour at Job I, and $30 an hour at Job II, how many hours should she work per week at each job to maximize her income?</p><h3 id="693e3ab4-8f26-41a4-bb68-a2bc43e000fb" class="">Solution</h3><ol type="1" id="9247b0e0-1dbe-44b8-a707-6e7997310408" class="numbered-list" start="1"><li><mark class="highlight-yellow_background"><strong>Set up the problem</strong></mark></li></ol><p id="2188904c-6606-4e58-b5fe-7bd9b336a017" class="">We denote the number of hours she should work per week at job I and job II are x1 and x2 respectively</p><p id="66cd0e03-86dd-424f-a9a1-6e41aeb561a6" class="">The objective function that we need to maximize is her income:
<strong>f(x1, x2) = 40x1 + 30x2 = Z</strong></p><p id="4e8418b5-60f9-4011-86c2-670dbe0619e6" class="">There are some constraints:</p><div id="b9c3d11f-2d5a-4e1d-b552-85a5924e9771" class="column-list"><div id="79cac05d-93b5-428a-9736-3f370c5652aa" style="width:50%" class="column"><ul id="a3018b76-7278-4977-a343-71f8f0a1d159" class="bulleted-list"><li style="list-style-type:disc">She never wants to work more than a total of 12 hours a week
<strong>x1 + x2 ≤ 12</strong></li></ul><ul id="538f98eb-b8db-40f1-a547-21c97da38a38" class="bulleted-list"><li style="list-style-type:disc">She has determined that for every hour she works at Job I, she needs 2 hours of preparation time, and for every hour she works at Job II, she needs one hour of preparation time, and she cannot spend more than 16 hours for preparation<p id="0067b8f0-22e0-4ac7-a05b-03d53fef53bd" class=""><strong>2x1 + x2 ≤ 16</strong></p></li></ul></div><div id="c3bffbeb-f6e8-41ad-9ec6-ca0568d2ef4f" style="width:50%" class="column"><figure id="9e0cffc4-1700-4979-801a-46461ca49405" class="image"><a href="SIMPLEX%20METHOD%209e0cffc417004979801a46461ca49405/Untitled.png"><img style="width:432px" src="SIMPLEX%20METHOD%209e0cffc417004979801a46461ca49405/Untitled.png"/></a></figure></div></div><ol type="1" id="ae5ed3fb-6530-466f-84fd-c5f20b2eac5b" class="numbered-list" start="2"><li><mark class="highlight-yellow_background"><strong>Convert the inequalities into equations (standard form)</strong></mark></li></ol><ul id="b9c239f2-a607-4c3f-aed4-ba710655359f" class="bulleted-list"><li style="list-style-type:disc">- 40x1 - 30x2 + Z = 0</li></ul><p id="9e6d3457-5c8f-4a4e-bbaa-c7b6d330754a" class="">We need to add 2 slack variables s1 &amp; s1 such that:</p><ul id="8b0589fb-6d8e-41d8-bed2-ba812e9ca4e2" class="bulleted-list"><li style="list-style-type:disc">x1 + x2 + s1 = 12</li></ul><ul id="6ef1fd7f-7d26-4001-8c9f-a99714da73a2" class="bulleted-list"><li style="list-style-type:disc">2x1 + x2 + s2 = 16</li></ul><ol type="1" id="7c9e96f5-5325-4601-a32a-80e7b7c415ab" class="numbered-list" start="3"><li><mark class="highlight-yellow_background"><strong>Construct the simplex tableau</strong></mark></li></ol><table id="f5f9d083-da31-475a-9b34-503065dd703b" class="simple-table"><tbody><tr id="57cc18d7-39f5-4426-be51-42b40162d1a8"><td id="EJF~">x1</td><td id="b=g[">x2</td><td id="HFme">s1</td><td id="icG}">s2</td><td id="nI^P">Z</td><td id="|gCR">C</td></tr><tr id="3cc031df-12db-49e8-b4f3-8cce88213ee6"><td id="EJF~">1</td><td id="b=g[">1</td><td id="HFme">1</td><td id="icG}">0</td><td id="nI^P">0</td><td id="|gCR">12</td></tr><tr id="f89822e8-0d47-4bbd-a3f2-dbead649caea"><td id="EJF~">2</td><td id="b=g[">1</td><td id="HFme">0</td><td id="icG}">1</td><td id="nI^P">0</td><td id="|gCR">16</td></tr><tr id="a5cb369a-5a59-445d-b18a-3b21228b50a3"><td id="EJF~">-40</td><td id="b=g[">-30</td><td id="HFme">0</td><td id="icG}">0</td><td id="nI^P">1</td><td id="|gCR">0</td></tr></tbody></table><p id="63813079-d1ca-4759-87cb-7224edaa00a4" class=""><mark class="highlight-yellow_background"><strong>The most negative entry in the bottom row identifies the pivot column.</strong></mark></p><p id="8fed42b6-bc3d-4b91-aa2b-17ae70a308f7" class="">As can easily be seen from the above tableau that the first column</p><ul id="4037fdb7-bf04-4441-a2a7-a9c30c971da9" class="toggle"><li><details open=""><summary><em><strong>Question:</strong></em> Why the most negative entry?</summary><p id="e6b9dbf0-df6d-4e3f-a191-173598d043a9" class="">Because it represents the largest coefficient of the objective function, the coefficient whose entry will increase the value of Z the quickest. </p><p id="9d103178-1678-408c-a0f8-4c22a354ec9f" class="">The simplex method begins at a corner point where all the main variables are zero. It then moves from a corner point to the adjacent corner point always increasing the value of the objective function. In the case of the objective function Z=40x1+30x2, it will make more sense to increase the value of x1 rather than x2</p></details></li></ul><ol type="1" id="7c1ee682-0523-44e1-ae44-6c55482ce0c5" class="numbered-list" start="5"><li><mark class="highlight-yellow_background"><strong>Define the quotient (thương số) and pivot element.</strong></mark></li></ol><table id="8c2df309-1106-4341-82be-a4c054aa5cd3" class="simple-table"><tbody><tr id="24c13a91-230b-48f8-8d6a-41c654a58d3d"><td id="EJF~">x1</td><td id="b=g[">x2</td><td id="HFme">s1</td><td id="icG}">s2</td><td id="nI^P">Z</td><td id="|gCR">C</td><td id="bDZB">Quotient</td></tr><tr id="24071a86-f7e9-499f-bfd7-a93dc5e65a10"><td id="EJF~">1</td><td id="b=g[">1</td><td id="HFme">1</td><td id="icG}">0</td><td id="nI^P">0</td><td id="|gCR">12</td><td id="bDZB">12/1 = 12</td></tr><tr id="b38463cc-a46f-4191-be14-96bfd7499df0"><td id="EJF~"><mark class="highlight-red">2</mark></td><td id="b=g[">1</td><td id="HFme">0</td><td id="icG}">1</td><td id="nI^P">0</td><td id="|gCR">16</td><td id="bDZB">16/2 = 8</td></tr><tr id="51b67f8f-d3c5-4858-b593-c95e4e905cad"><td id="EJF~">-40</td><td id="b=g[">-30</td><td id="HFme">0</td><td id="icG}">0</td><td id="nI^P">1</td><td id="|gCR">0</td><td id="bDZB"></td></tr></tbody></table><ul id="e7652cca-8fdd-4757-93e7-11aa4ec4bed1" class="toggle"><li><details open=""><summary><em><strong>Question</strong></em> Why do we find quotients, and why does the smallest quotient identify a row?</summary><p id="ee69a0bb-db7e-4650-b64c-af2afdee07bb" class="">When we choose the most negative entry in the bottom row, we are trying to increase the value of the objective function by bringing in the variable x1. But we cannot choose any value for x1, using the quotients to identify the pivot element guarantees that we do not violate the constraints.</p></details></li></ul><ul id="dc3bdbbd-8744-4624-850c-bfce27455a31" class="toggle"><li><details open=""><summary><em><strong>Question</strong></em> Why do we identify the pivot element?</summary><p id="34e44187-d10d-49ba-b872-9eb3f6142a84" class=""><em><strong>Answer</strong></em> As we have mentioned earlier, the simplex method begins with a corner point and then moves to the next corner point always improving the value of the objective function. The value of the objective function is improved by changing the number of units of the variables. We may add the number of units of one variable, while throwing away the units of another. Pivoting allows us to do just that.</p><p id="32828369-12f5-4ad5-864f-a43260e9f353" class="">The variable whose units are being added is called the <strong>entering variable,</strong> and the variable whose units are being replaced is called the <strong>departing variable</strong>. The entering variable in the above table is x1, and it was identified by the most negative entry in the bottom row. The departing variable s2 was identified by the lowest of all quotients.</p></details></li></ul><ol type="1" id="24ca11e8-92bc-4b31-996b-54615892f6bc" class="numbered-list" start="6"><li><mark class="highlight-yellow_background"><strong>Perform pivoting to make all other entries in this column zero. </strong></mark></li></ol><ul id="d33b2af8-1146-4b9f-9117-3274a41c38ca" class="bulleted-list"><li style="list-style-type:disc">At the beginning</li></ul><table id="cb39af67-20c7-42e8-b9bc-7446f6515316" class="simple-table"><tbody><tr id="932230bc-d651-4176-a97a-eae23d9a3cb2"><td id="EJF~">x1</td><td id="b=g[">x2</td><td id="HFme">s1</td><td id="icG}">s2</td><td id="nI^P">Z</td><td id="|gCR">C</td></tr><tr id="d48ce767-2456-4277-b83a-31d308f6a40f"><td id="EJF~">1</td><td id="b=g[">1</td><td id="HFme">1</td><td id="icG}">0</td><td id="nI^P">0</td><td id="|gCR">12</td></tr><tr id="0db2febf-53c1-447d-be88-5fe38dce305e"><td id="EJF~">2</td><td id="b=g[">1</td><td id="HFme">0</td><td id="icG}">1</td><td id="nI^P">0</td><td id="|gCR">16</td></tr><tr id="098ffe17-730c-4aa6-84e4-31d9a487982f"><td id="EJF~">-40</td><td id="b=g[">-30</td><td id="HFme">0</td><td id="icG}">0</td><td id="nI^P">1</td><td id="|gCR">0</td></tr></tbody></table><p id="fd39dfd2-336c-441c-b46a-7add451c6a80" class="">The corresponding solution is x1 = x2 = 0, s1 = 12, s2 = 16</p><div id="bce0e06d-f6d2-4b5d-951e-d40ae4c2d62c" class="column-list"><div id="002d2f4b-8aa7-4e56-8bbd-bbaff834d8e0" style="width:50%" class="column"><p id="9c9ff7d2-2290-466d-b964-171d3ac9c657" class="">x1 + x2 + s1 = 12</p><p id="9c98808d-d36a-456c-adcc-3387c7618809" class="">2x1 + x2 + s2 = 16</p><p id="fce0342c-054b-4ca7-976e-44b0dee8baac" class="">Z = 40x1 + 30x2</p></div><div id="42aefeed-4abe-4577-a2ad-63d76837916e" style="width:50%" class="column"><p id="c2cbae4a-bbf0-4ce9-858d-12eb4aaa5d5c" class="">s1 = 12 - x1 - x2</p><p id="783dc274-0ad7-437e-b069-605a25a09896" class="">s2 =  16 - 2x1 - x2</p><p id="41f13bba-80f8-4837-9664-fc3bc397999c" class="">Z = 40x1 + 30x2</p></div></div><ul id="adeb7816-85b8-4f08-b22a-091beb6c22f6" class="bulleted-list"><li style="list-style-type:disc">Change pivot into 1 and do row elimination operations</li></ul><table id="599cf1dc-165e-4962-a76a-1fa33ee84761" class="simple-table"><tbody><tr id="6dd5374b-9536-4ec7-8e13-11d47860d28e"><td id="EJF~">x1</td><td id="b=g[">x2</td><td id="HFme">s1</td><td id="icG}">s2</td><td id="nI^P">Z</td><td id="|gCR">C</td></tr><tr id="831ab738-111e-419d-9f2a-910b840bcf68"><td id="EJF~">1</td><td id="b=g[">1</td><td id="HFme">1</td><td id="icG}">0</td><td id="nI^P">0</td><td id="|gCR">12</td></tr><tr id="f7a6342d-228b-4f73-875b-47c07c9cad85"><td id="EJF~">1</td><td id="b=g[">1/2</td><td id="HFme">0</td><td id="icG}">1/2</td><td id="nI^P">0</td><td id="|gCR">8</td></tr><tr id="a8fba4e3-5513-4cf1-b20a-1dab20a8f0dc"><td id="EJF~">-40</td><td id="b=g[">-30</td><td id="HFme">0</td><td id="icG}">0</td><td id="nI^P">1</td><td id="|gCR">0</td></tr></tbody></table><p id="23f4fc1c-a054-4416-b9c8-bfb712cbef13" class="">x1 is the entering value and s2 is the departing value</p><div id="09e19bb6-80a1-48d2-8182-724789323a96" class="column-list"><div id="59558b66-6c28-4763-b42c-329e68e9235e" style="width:50%" class="column"><p id="5be1d0e4-b6e3-477b-a684-8134c8606eb3" class="">s1 = 12 - (-s2/2-x2/2+8) - x2</p><p id="e71f1d95-a59d-4fce-add8-2cfabc274eb6" class="">x1 = -s2/2 - x2/2 + 8</p><p id="6496a140-3978-4cba-b5cf-4d1cfd495627" class="">Z = 40(-s2/2 - x2/2 + 8) + 30x2</p></div><div id="55c4c09e-ff00-4c83-bae8-8244d25bab2c" style="width:50%" class="column"><p id="d3991376-1f17-40b4-8786-cd857922c2cd" class="">s1 = 4 + s2/2 - x2/2</p><p id="c4b1019a-8445-4d12-9cad-4e41dc1ef734" class="">x1 = -s2/2 - x2/2 + 8</p><p id="7422c495-a9ce-49ee-bfd0-5465a31b70b1" class="">Z = 320 + 10x2 -20s2</p></div></div><p id="d5d94999-5411-401e-9f54-e18bd68f6d32" class="">Basic solution is x1 = 8, x2 = 0, s2 = 0, s1 = 4, Z = 320</p><table id="4d5fbda8-5ab8-4458-a1a4-747f05167094" class="simple-table"><tbody><tr id="44035752-ce15-49ee-8bdc-fffc8e746f52"><td id="EJF~">x1</td><td id="b=g[">x2</td><td id="HFme">s1</td><td id="icG}">s2</td><td id="nI^P">Z</td><td id="|gCR">C</td></tr><tr id="f1ba21b4-fe7e-4919-9fb5-764e3d3ff100"><td id="EJF~">0</td><td id="b=g[">1/2</td><td id="HFme">1</td><td id="icG}">-1/2</td><td id="nI^P">0</td><td id="|gCR">4</td></tr><tr id="de916dfa-5777-42cd-ae31-6d1b7f70ec8b"><td id="EJF~">1</td><td id="b=g[">1/2</td><td id="HFme">0</td><td id="icG}">1/2</td><td id="nI^P">0</td><td id="|gCR">8</td></tr><tr id="b796d9e3-d1a8-40f4-9f57-e0635c8d9b8b"><td id="EJF~">0</td><td id="b=g[">-10</td><td id="HFme">0</td><td id="icG}">20</td><td id="nI^P">1</td><td id="|gCR">320</td></tr></tbody></table><ol type="1" id="a272c8b0-4fcb-4db9-bb37-f1b84b07902a" class="numbered-list" start="7"><li><mark class="highlight-yellow_background"><strong>When there are no more negative entries in the bottom row, we are finished; otherwise, we start again from step 4.</strong></mark></li></ol><table id="af8ba490-b41a-4d2f-a532-d51ceffe4b79" class="simple-table"><tbody><tr id="c8e101f3-23d4-4be4-9163-546d74739139"><td id="EJF~">x1</td><td id="b=g[">x2</td><td id="HFme">s1</td><td id="icG}">s2</td><td id="nI^P">Z</td><td id="|gCR">C</td></tr><tr id="d21450ce-f655-4716-ab39-afee2b8a6660"><td id="EJF~">0</td><td id="b=g["><mark class="highlight-red">1/2</mark></td><td id="HFme">1</td><td id="icG}">-1/2</td><td id="nI^P">0</td><td id="|gCR">4</td></tr><tr id="f4d78c6f-dad6-485d-aff2-b9364216af34"><td id="EJF~">1</td><td id="b=g[">1/2</td><td id="HFme">0</td><td id="icG}">1/2</td><td id="nI^P">0</td><td id="|gCR">8</td></tr><tr id="96d98eb5-70d0-44e3-a4f4-d07612e325fe"><td id="EJF~">0</td><td id="b=g["><mark class="highlight-red">-10</mark></td><td id="HFme">0</td><td id="icG}">20</td><td id="nI^P">1</td><td id="|gCR">320</td></tr></tbody></table><p id="e57e91fe-652c-43ea-9581-21ebc3224733" class="">x2 is the entering value and s1 is the departing value</p><div id="849a9604-0677-41fb-bc56-ead996d4fa01" class="column-list"><div id="4bc60cce-692c-49a3-bd6c-4828b9db2034" style="width:50%" class="column"><p id="b281b1d8-2368-4109-82a8-f3ebf7ea95ce" class="">x2 = 8 + s2 - 2s1</p><p id="bd8e428b-85b9-4567-89ce-ce7902ae91fe" class="">x1 = -s2/2 - (4 + s2/2 - s1) + 8</p><p id="19bb478a-8162-43a0-816e-124988b48105" class="">Z = 320 + 10(8 + s2 - 2s1) -20s2</p></div><div id="8c61e136-d88d-46ea-b688-605ee0f7e22f" style="width:50%" class="column"><p id="cf82f6aa-ad56-4748-91e7-b7ed57bd4deb" class="">x2 = 8 + s2 - 2s1</p><p id="93b609ea-c10b-4f25-a8b1-53c6be506b49" class="">x1 =  -s2 + s1 + 4</p><p id="3852303b-2e3c-437a-831c-39351fbd6230" class="">Z = 400 - 10s2 - 20s1</p></div></div><table id="12cd62be-451e-4f36-a3e5-ad6847f8e4f4" class="simple-table"><tbody><tr id="4ebcd4dd-959d-4825-8361-f4af17e961ab"><td id="EJF~">x1</td><td id="b=g[">x2</td><td id="HFme">s1</td><td id="icG}">s2</td><td id="nI^P">Z</td><td id="|gCR">C</td></tr><tr id="6dbfe162-0693-44b0-8ad9-829d30e0f62a"><td id="EJF~">0</td><td id="b=g["><mark class="highlight-red">1/2</mark></td><td id="HFme">1</td><td id="icG}">-1/2</td><td id="nI^P">0</td><td id="|gCR">4</td></tr><tr id="396eb4f0-5e0b-4c99-a38c-d4b14fbdb5fe"><td id="EJF~">1</td><td id="b=g[">0</td><td id="HFme">-1</td><td id="icG}">1</td><td id="nI^P">0</td><td id="|gCR">4</td></tr><tr id="24f7cb36-5738-445b-bcef-c1713d95e289"><td id="EJF~">0</td><td id="b=g[">0</td><td id="HFme">20</td><td id="icG}">10</td><td id="nI^P">1</td><td id="|gCR">400</td></tr></tbody></table><p id="c574e088-c6e1-4a25-8929-c3c4489b09df" class="">Basic solution is x1 = 4, x2 = 8, Z = 400</p><ol type="1" id="d669502f-ea6a-4539-bc41-534b174c223f" class="numbered-list" start="8"><li><mark class="highlight-yellow_background"><strong>Read off the answer:</strong></mark></li></ol><table id="75562175-3efe-4e01-ab76-df4e19a9fb54" class="simple-table"><tbody><tr id="29a37a47-0bdf-4119-af3f-73d94bec9f4d"><td id="`ruu">x1</td><td id=":wzb">x2</td><td id="qtBB">Z</td><td id="Mn?m">C</td></tr><tr id="690cf849-d809-4ed7-9504-ace67d984d9f"><td id="`ruu">0</td><td id=":wzb">1</td><td id="qtBB">0</td><td id="Mn?m">8</td></tr><tr id="3fc2a01e-3fad-4985-b2f6-5274e9d4765b"><td id="`ruu">1</td><td id=":wzb">0</td><td id="qtBB">0</td><td id="Mn?m">4</td></tr><tr id="28a03ec2-ca14-4b41-a165-5273d2610e52"><td id="`ruu">0</td><td id=":wzb">0</td><td id="qtBB">1</td><td id="Mn?m"><mark class="highlight-red">400</mark></td></tr></tbody></table><h3 id="7d1bbe4a-3bfe-45e4-8bd9-ef06761e41c7" class=""><strong>So, the solution is x1 = 8, x2 = 4 and maximum income is 400.</strong></h3><p id="c18d386e-bfd5-418d-aeb7-71bf7d56e0f1" class="">
</p></div></article></body></html>
