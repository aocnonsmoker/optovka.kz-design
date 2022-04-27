<template>
	<div class="home">
		<div class="container">
			<div class="row">
				<div class="col-sm-3">
					<div class="left-sidebar">
						<h2>Category</h2>
						<div class="accordion" role="tablist">
							<b-card no-body class="mb-1">
								<b-card-header header-tag="header" class="p-1" role="tab">
									<b-button block v-b-toggle.accordion-1 class="category-item">Accordion 1</b-button>
								</b-card-header>
								<b-collapse id="accordion-1" accordion="my-accordion" role="tabpanel">
									<b-card-body>
										<div class="accordion" role="tablist">
											<b-card no-body>
												<b-card-header header-tag="header" class="p-1" role="tab">
													<b-button block v-b-toggle.accordion-2 class="category-item">Child 1</b-button>
												</b-card-header>
												<b-collapse id="accordion-2" accordion="my-accordion2" role="tabpanel">
													<b-card-body>
														<b-card-text>{{ text }}</b-card-text>
													</b-card-body>
												</b-collapse>
											</b-card>

											<b-card no-body class="mb-1">
												<b-card-header header-tag="header" class="p-1" role="tab">
													<b-button block class="category-item">Child 2</b-button>
												</b-card-header>
											</b-card>

											<b-card no-body class="mb-1">
												<b-card-header header-tag="header" class="p-1" role="tab">
													<b-button block class="category-item">Child 3</b-button>
												</b-card-header>
											</b-card>
										</div>
									</b-card-body>
								</b-collapse>
							</b-card>

							<b-card no-body>
								<b-card-header header-tag="header" class="p-1" role="tab">
									<b-button block class="category-item">Accordion 2</b-button>
								</b-card-header>
							</b-card>

							<b-card no-body>
								<b-card-header header-tag="header" class="p-1" role="tab">
									<b-button block v-b-toggle.accordion-3 class="category-item">Accordion 3</b-button>
								</b-card-header>
								<b-collapse id="accordion-3" accordion="my-accordion" role="tabpanel">
									<b-card-body>
										<b-card-text>{{ text }}</b-card-text>
									</b-card-body>
								</b-collapse>
							</b-card>
						</div>
					</div>
				</div>
				<div class="col-sm-9 padding-right">
					<h2 class="title text-center">Features Items</h2>
					<div class="row">
						<div v-for="item in 6" :key="item" class="col-sm-4">
							<div class="product-image-wrapper">
								<div class="single-products">
									<div class="productinfo text-center">
										<img src="../assets/product1.jpg" alt="">
										<h2>$56</h2>
										<p>Easy Polo Black Edition</p>
										<a href="#" class="btn btn-default add-to-cart"><font-awesome-icon class="icon" icon="shopping-cart" /> Add to cart</a>
									</div>
									<div class="product-overlay">
										<div class="overlay-content">
											<h2>$56</h2>
											<p>Easy Polo Black Edition</p>
											<a href="#" class="btn btn-default add-to-cart"><font-awesome-icon class="icon" icon="shopping-cart" /> Add to cart</a>
										</div>
									</div>
								</div>
								<div class="choose"></div>
							</div>
						</div>
					</div>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
export default {
  name: 'Home',
  data() {
	return {
		text: 'Some a lot of text'
	}
  }
}
</script>

<style scoped>
	.left-sidebar h2,
	.brands_products h2 {
		color: #FE980F;
		font-family: 'Roboto', sans-serif;
		font-size: 18px;
		font-weight: 700;
		margin: 0 auto 30px;
		text-align: center;
		text-transform: uppercase;
		position: relative;
		z-index: 3;
	}

	.left-sidebar h2:after,
	h2.title:after {
		content: " ";
		position: absolute;
		border: 1px solid #f5f5f5;
		bottom: 8px;
		left: 0;
		width: 100%;
		height: 0;
		z-index: -2;
	}

	.left-sidebar h2:before {
		content: " ";
		position: absolute;
		background: #fff;
		bottom: -6px;
		width: 130px;
		height: 30px;
		z-index: -1;
		left: 50%;
		margin-left: -65px;
	}

	.category-item {
		background-color: white;
		border: 0;
		color: #FE980F;
	}

	.not-collapsed {
		background-color: #FE980F;
		color: black;
	}

	h2.title {
		color: #FE980F;
		font-family: 'Roboto', sans-serif;
		font-size: 18px;
		font-weight: 700;
		margin: 0 15px;
		text-transform: uppercase;
		margin-bottom: 30px;
		position: relative;
	}

	.product-image-wrapper {
		border: 1px solid #F7F7F5;
		overflow: hidden;
		margin-bottom: 30px;
	}

	.padding-right {
		padding-right: 0;
	}

	.single-products {
		position: relative;
	}

	.productinfo h2 {
		color: #FE980F;
		font-family: 'Roboto', sans-serif;
		font-size: 24px;
		font-weight: 700;
	}

	.overlay-content h2 {
		color: white;
		font-family: 'Roboto', sans-serif;
		font-size: 24px;
		font-weight: 700;
	}

	.productinfo p {
		font-family: 'Roboto', sans-serif;
		font-size: 14px;
		font-weight: 400;
		color: #696763;
	}

	.productinfo img {
		width: 100%;
	}

	.productinfo {
		position: relative;
	}

	.product-overlay {
		background: rgba(254, 152, 15, .8);
		top: 0;
		display: none;
		height: 0;
		position: absolute;
		-webkit-transition: height 500ms ease 0s;
		transition: height 500ms ease 0s;
		width: 100%;
		display: block;
	}

	.single-products:hover .product-overlay {
		display: block;
		height: 100%;
	}

	.product-overlay .overlay-content {
		bottom: 0;
		position: absolute;
		bottom: 0;
		text-align: center;
		width: 100%;
	}

	.product-overlay .add-to-cart {
		background: #fff;
		border: 0 none;
		border-radius: 0;
		color: #FE980F;
		font-family: 'Roboto', sans-serif;
		font-size: 15px;
		margin-bottom: 25px;
	}

	.product-overlay .add-to-cart:hover {
		background: #fff;
		color: #FE980F;
	}

	.product-overlay p {
		font-family: 'Roboto', sans-serif;
		font-size: 14px;
		font-weight: 400;
		color: #fff;
	}

	.add-to-cart {
		background: #F5F5ED;
		border: 0 none;
		border-radius: 0;
		color: #696763;
		font-family: 'Roboto', sans-serif;
		font-size: 15px;
		margin-bottom: 25px;
	}

	.add-to-cart:hover {
		background: #FE980F;
		border: 0 none;
		border-radius: 0;
		color: #FFFFFF;
	}

	.icon {
		margin-right: 5px;
	}

	.add-to-cart:hover {
		background: #FE980F;
		color: #FFFFFF;
	}

	.choose {
		border-top: 1px solid #F7F7F0;
	}

	.choose ul li a {
		color: #B3AFA8;
		font-family: 'Roboto', sans-serif;
		font-size: 13px;
		padding-left: 0;
		padding-right: 0;
	}

	.choose ul li a i {
		margin-right: 5px;
	}

	.choose ul li a:hover {
		background: none;
		color: #FE980F;
	}
</style>
