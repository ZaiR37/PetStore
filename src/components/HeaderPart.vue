<template>
	<header>
		<div class="header-container">
			<div class="logo">
				<a href="#home">
					<img src="../assets/icons/petShop-logo.webp" alt="petShop-logo" />
				</a>
			</div>
			<form action="" method="get" name="simpleSearch" novalidat class="searchBar-wrapper">
				<input type="text" name="searchbar" id="searchbar" placeholder="Search" />
				<button type="submit">
					<img src="../assets/icons/search-icon.svg" alt="search-icon" />
				</button>
			</form>
			<div class="signIn">
				<a href="#SignIn" id="signInLink">
					Sign In
					<img src="../assets/icons/chevron-up.svg" alt="chevron-up" />
				</a>
				<div class="signUp-box">
					<span>Don't have an acount ?
						<a href="#SignUp" id="signUpLink">Sign Up</a> now!</span>
				</div>
			</div>
			<div class="cart">
				<a href="#cart">
					<img src="../assets/icons/cart-icon.svg" alt="cart">
				</a>
			</div>
		</div>
	</header>
</template>

<script>

</script>

<style>
/* === HEADER === */
header {
	margin: 0;
	padding: 10px;

	font-family: "Poppins", sans-serif;
}

.header-container {
	display: flex;
	justify-content: space-around;
	align-items: center;
	gap: 5px;

	margin: auto;
	max-width: 1100px;
}

/* --- LOGO --- */

.logo img {
	width: 150px;
	height: auto;
}

/* --- SEARCHBAR --- */

.searchBar-wrapper {
	display: flex;
	flex-shrink: 2;
	height: 40px;
	width: min(50%, 700px);
}

.searchBar-wrapper input[type="text"] {
	font-size: medium;

	width: 100%;

	border: 1px solid #33333378;
	border-right: none;
	border-radius: 2px 0 0 2px;
}

.searchBar-wrapper button {
	width: min(100%, 60px);

	border: 1px solid #33333378;
	border-left: none;
	border-radius: 0 2px 2px 0;
}

.searchBar-wrapper button img {
	width: 20px;
	height: auto;
}

/* --- SIGN UP DROPDOWN BOX --- */
.signUp-box {
	position: absolute;

	right: 0;
	top: 30px;
	margin: 5px;
	padding: 5px;
	width: 166px;

	font-size: 0.9rem;
	background-color: rgb(240, 240, 240);
	border: 1px solid rgb(218, 218, 218);
	box-shadow: rgba(50, 50, 93, 0.25) 0px 2px 5px -1px,
		rgba(0, 0, 0, 0.3) 0px 1px 3px -1px;

	visibility: hidden;
	opacity: 0;
	transition: visibility 0s, opacity 0.5s linear;
}

.signUp-box #signUpLink {
	color: black;
	font-size: 1.1rem;
	font-weight: 600;
	text-decoration: none;
}

/* --- SIGN IN --- */

.signIn {
	position: relative;
	min-width: 85px;
	height: 34px;
	text-align: center;
}

.signIn #signInLink {
	color: black;
	font-size: 1.1rem;
	font-weight: 600;
	text-decoration: none;

	display: block;
	height: 100%;
}

.signIn img {
	width: 20px;
	height: auto;

	transition: transform 0.15s linear;
}

.signUp-box a {
	display: inline;
}

.signIn:hover img {
	transform: rotate(180deg);
}

.signIn:hover #signInLink {
	color: rgb(138, 138, 138);
}

.signIn:hover img {
	filter: invert(50%);
}

.signIn:hover .signUp-box {
	visibility: visible;
	opacity: 1;
}

.signIn #signInLink:active {
	color: rgb(204, 204, 204);
}

.signIn #signInLink:active img {
	filter: invert(80%);
}

.signUp-box #signUpLink:hover {
	color: rgb(68, 0, 255);
}

.signUp-box #signUpLink:active {
	color: rgb(158, 124, 250);
}

/* --- CART --- */


.cart img {
	width: 32px;
	height: auto;

	vertical-align: middle;

	stroke-width: 10px;
	stroke: blue;
}

.cart a {
	display: block;
}

.cart a:hover img {
	stroke: red;
}

@media all and (max-width: 700px) {
	.header-container {
		flex-wrap: wrap;
	}

	/* --- LOGO --- */
	.logo {
		margin-bottom: 20px;
		flex-basis: 700px;
	}

	.logo a {
		display: block;
	}

	.logo img {
		display: block;
		margin: auto;
		width: min(100%, 200px);
		height: auto;
	}

	/* --- SEARCHBAR --- */

	.searchBar-wrapper {
		flex-grow: 1;
	}

	/* --- SIGNIN & CART --- */
	.signIn, .cart {
		display: none;
	}
}
</style>