<template>
    <footer id="footer">
        <div class="footer-bottom">
			<div class="container">
				<div class="row">
					<p class="pull-left text-left">Copyright © 2020 Optovka.kz | All rights reserved.</p>
					<p class="pull-right text-right">Developed by Zhambyl Kairken</p>
				</div>
			</div>
		</div>
    </footer>
</template>

<style scoped>
    #footer {
        background: #F0F0E9;
    }
    .container {
        border-bottom: 1px solid #E0E0DA;
        padding-bottom: 10px;
    }
    .footer-bottom {
        background: #D6D6D0;
        padding-top: 10px;
    }

    .footer-bottom p {
        color: #363432;
        font-family: 'Roboto', sans-serif;
        font-weight: 300;
        margin-left: 15px;
    }

    .pull-right {
        float: right !important;
    }

    .pull-left {
        float: left !important;
    }

    .row {
        display: inline;
    }
</style>