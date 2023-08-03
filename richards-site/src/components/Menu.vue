<template>
	<!-- menu section -->
	<section class="menu-container" id="menu-section">
		<div class="menu-box">
			<div class="sauces">
				<div id="plats-jour">
					<img src="../assets/menu-line-flip.png" alt="">
					<h2 class="menu-title">PLATS DU JOUR</h2>
					<img src="../assets/menu-line.png" alt="">
				</div>
				<div class="menu-item">
					<p class="item-title">Club Sandwich au poulet</p>
					<p class="item-description">
						Sandwich savoureux et généreux, idéal pour un déjeuner gourmand.
					</p>
				</div>

				<div class="menu-item">
					<p class="item-title">Club Sandwich au saumon</p>
					<p class="item-description">
						Sandwich savoureux et généreux, idéal pour un déjeuner gourmand.
					</p>
				</div>
				<div class="menu-item">
					<p class="item-title">Club Sandwich au poulet</p>
					<p class="item-description">
						Sandwich savoureux et généreux, idéal pour un déjeuner gourmand.
					</p>
				</div>
				<div class="menu-item">
					<p class="item-title">Club Sandwich au saumon</p>
					<p class="item-description">
						Sandwich savoureux et généreux, idéal pour un déjeuner gourmand.
					</p>
				</div>
				<div class="menu-item">
					<p class="item-title">Club Sandwich au poulet</p>
					<p class="item-description">
						Sandwich savoureux et généreux, idéal pour un déjeuner gourmand.
					</p>
				</div>
			</div>
			<a class="btn btn-menu" @click="showModal">VOIR MENU COMPLET</a>

			<!-- MODAL -->
			<div
				:class="{ 'modal-background': modalVisible }"
				@click="closeModal"
			></div>
			<modal id="modal" class="modal" :visible="modalVisible">
				<div class="modal-close-container" @click="closeModal">
					<div class="modal-close"></div>
				</div>
				<h2 class="modal-title">DISPONIBLE TOUS LES JOURS DE LA SEMAINE</h2>
				<div class="modal-menu">
					<!-- SAUCES -->
					<div class="sauces">
						<div id="plats-jour">
					<img src="../assets/menu-line-flip.png" alt="">
					<h2 class="menu-title">PLATS DU JOUR</h2>
					<img src="../assets/menu-line.png" alt="">
				</div>

				<div class="menu-item-modal">
					<div class="item-title-container">
						<p class="item-title">Club Sandwich au poulet</p>
						<div id="separator-menu"></div>
						<p class="item-price">5000 CFA</p>
						</div>
					<p class="item-description">
						Sandwich savoureux et généreux, idéal pour un déjeuner gourmand.
					</p>
				</div>
				<div class="menu-item-modal">
					<div class="item-title-container">
						<p class="item-title">Club Sandwich au poulet</p>
						<div id="separator-menu"></div>
						<p class="item-price">5000 CFA</p>
						</div>
					<p class="item-description">
						Sandwich savoureux et généreux, idéal pour un déjeuner gourmand.
					</p>
				</div>
				<div class="menu-item-modal">
					<div class="item-title-container">
						<p class="item-title">Club Sandwich au poulet</p>
						<div id="separator-menu"></div>
						<p class="item-price">5000 CFA</p>
						</div>
					<p class="item-description">
						Sandwich savoureux et généreux, idéal pour un déjeuner gourmand.
					</p>
				</div>
				<div class="menu-item-modal">
					<div class="item-title-container">
						<p class="item-title">Club Sandwich au poulet</p>
						<div id="separator-menu"></div>
						<p class="item-price">5000 CFA</p>
						</div>
					<p class="item-description">
						Sandwich savoureux et généreux, idéal pour un déjeuner gourmand.
					</p>
				</div>
				<div class="menu-item-modal">
					<div class="item-title-container">
						<p class="item-title">Club Sandwich au poulet</p>
						<div id="separator-menu"></div>
						<p class="item-price">5000 CFA</p>
						</div>
					<p class="item-description">
						Sandwich savoureux et généreux, idéal pour un déjeuner gourmand.
					</p>
				</div>
					</div>
				</div>
			</modal>

		</div>
	</section>
	<!-- menu section -->
</template>

<script>
import Modal from "./Modal.vue";

export default {
	name: "Menu",
	props: {
		showModal: Boolean,
	},
	components: {
		Modal,
	},
	data() {
		return {
			modalVisible: false,
		};
	},
	methods: {
		showModal() {
			this.modalVisible = true;
		},
		closeModal() {
			this.modalVisible = false;
		},
	},
};
</script>
<style scoped>
@import "../style.css";
</style>
