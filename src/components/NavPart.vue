<template>
	<nav>
		<button class="menuButton">
			Menu
			<img src="../assets/icons/menu-icon.svg" alt="menu-icon">
		</button>

		<ul class="nav-container">
			<li class="navContent signNCart">
				<a href="">
					Sign In
					<img src="../assets/icons/petSupplies-icon.svg" alt="petSupplies-icon" id="petSupplies-icon">
				</a>

				<a href="">
					<img src="../assets/icons/cart-icon.svg" alt="petSupplies-icon" id="petSupplies-icon">
				</a>
			</li>

			<li class="navContent">
				<a href="#petSupplies">
					Pet Supplies
					<img src="../assets/icons/petSupplies-icon.svg" alt="petSupplies-icon" id="petSupplies-icon">

				</a>
			</li>
			<li class="navContent">
				<a href="#petService">
					Pet Service
					<img src="../assets/icons/petService-icon.svg" alt="petService-icon" id="petService-icon">
				</a>
			</li>
			<li class="navContent">
				<a href="#petClinic">
					Pet Clinic
					<img src="../assets/icons/pharmacy-icon.svg" alt="petClinic-icon" id="petClinic-icon">
				</a>
			</li>
			<li class="navContent">
				<a href="#about">
					About
					<img src="../assets/icons/about-icon.svg" alt="about-icon" id="about-icon">
				</a>
			</li>
		</ul>
	</nav>
</template>

<script>

</script>

<style>
nav {
	padding: 3px 2px 0px 3px;
	font-family: "Poppins", sans-serif;
	background-color: #0f5bdd;
}

.menuButton {
	display: none;
}

.nav-container {
	display: flex;
	margin: auto;
	padding: 0;

	max-width: 1100px;
	list-style-type: none;

}

.nav-container .signNCart {
	display: none;
}

.navContent {

	color: white;
	flex-grow: 1;
	text-align: center;
}


.navContent a {
	margin: 5px 2px 5px 2px;
	display: block;
	padding: 0px;
	border-radius: 3px;

	color: white;
	font-size: 1.2rem;
	font-weight: 500;
	text-decoration: none;

}

.navContent a img {
	height: auto;
	width: 50px;
	margin-left: 10px;
	vertical-align: middle;

}


.navContent a:visited {
	color: white;
}

.navContent a:hover {
	background-color: rgba(0, 0, 0, 0.096);
}

.navContent a:active {
	background-color: rgba(0, 0, 0, 0.253);
}

@media all and (max-width: 700px) {
	nav {
		width: 98.5vw;
		overflow: hidden;
	}

	.nav-container {
		position: relative;
		flex-direction: column;
		display: none;
	}

	.menuButton {
		border: none;
		background-color: #0f5bdd;
		color: white;
		height: 40px;
		width: 100%;
		font-size: 1.1rem;
		font-weight: 600;
	}

	.menuButton:hover {
		background-color: #0000001a;
	}

	.menuButton:active {
		background-color: #0000002f;
	}

	.menuButton img {
		height: auto;
		width: 30px;
		vertical-align: middle;
		margin-left: 5px;
	}


	.menuButton:focus+.nav-container {
		display: block;
	}

	.nav-container:hover {
		display: block;
	}
}
</style>