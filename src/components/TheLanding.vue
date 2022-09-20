<template>
    <div class="container">
        <section class="banner">
            <div class="content">
                <h1>{{ title }}</h1>
                <p>{{ description }}</p>
                <a href="/about" class="start">
                    {{ button }}
                    <svg width="16px" height="13px" viewBox="0 0 16 13" fill="currentColor" xmlns="http://www.w3.org/2000/svg">
                        <path fill-rule="evenodd" clip-rule="evenodd" d="M8.35225 0.898347C8.82088 0.429718 9.58068 0.429718 10.0493 0.898347L14.8493 5.69835C15.3179 6.16698 15.3179 6.92677 14.8493 7.3954L10.0493 12.1954C9.58068 12.664 8.82088 12.664 8.35225 12.1954C7.88362 11.7268 7.88363 10.967 8.35225 10.4983L11.1037 7.74688L2.00078 7.74688C1.33804 7.74688 0.800781 7.20962 0.800781 6.54688C0.800781 5.88413 1.33804 5.34688 2.00078 5.34688H11.1037L8.35225 2.5954C7.88363 2.12677 7.88363 1.36698 8.35225 0.898347Z" fill="currentColor"></path>
                    </svg>
                </a>
            </div>
        </section>

		<section class="trust">
			<h2>
				Unsere Partner
			</h2>

			<div class="companies">
				<img lazy src="@/assets/skyscannerr-logo.svg" alt="skyscanner" />
				<img lazy src="@/assets/booking-logo.svg" alt="booking" />
				<img lazy src="@/assets/hostelworld-logo.svg" alt="hostelworld" />
				<img lazy src="@/assets/gyg-logo.svg" alt="gyg" />
				<img lazy src="@/assets/distribution-logo.svg" alt="distribution" />
			</div>
		</section>

		<section class="options">
			<h2 class="title">
				Als Backpacker kennst du sicherlich diese Probleme...
			</h2>

			<div class="items">
				<div class="item">
					<img lazy src="@/assets/fire-icon.svg" alt="Fehlende Inspiration" width="80" />
					<p>
						Fehlende Inspiration
					</p>
				</div>
				<div class="item">
					<img lazy src="@/assets/time-icon.svg" alt="Keine Zeit für die Planung" width="66" />
					<p>
						Keine Zeit für die Planung
					</p>
				</div>
				<div class="item">
					<img lazy src="@/assets/ticket-icon.svg" alt="Buchungsschwierigkeiten Kein" width="66" />
					<p>
						Buchungsschwierigkeiten Kein
					</p>
				</div>
				<div class="item">
					<img lazy src="@/assets/group-icon.svg" alt="Travel-Buddy" width="73" />
					<p>
						Travel-Buddy
					</p>
				</div>
			</div>
		</section>

		<section class="feature feature--create">
			<div class="image image--desktop">
				<img alt="Erstelle individuelle Reiserouten in nur wenigen Schritten." lazy src="@/assets/feature-c1.png" />
			</div>

			<div class="info">
				<p class="title">
					<span class="text-bl">
						Erstelle
					</span>
					individuelle
					<br />
					Reiserouten in nur
					<br />
					wenigen Schritten.
				</p>

				<img class="image image--mobile" alt="Erstelle individuelle Reiserouten in nur wenigen Schritten." lazy src="@/assets/feature-c1.png" />

				<p class="sub-title">
					Lästige Reiseplanung war gestern. Unsere WebApp
					<br />
					erstellt dir deine individuell angepasste Reiseroute - je nach Interessen und Budget.
				</p>

				<ul>
					<li>
						<img lazy alt="Check mark icon" src="@/assets/checkmark-icon.svg" width="15" />
						Entdecke neue Orte
					</li>
					<li>
						<img lazy alt="Check mark icon" src="@/assets/checkmark-icon.svg" width="15" />
						Gib Reisezeitraum und Budget an
					</li>
					<li>
						<img lazy alt="Check mark icon" src="@/assets/checkmark-icon.svg" width="15" />
						Finde die besten Reiserouten in deinem Reiseziel
					</li>
				</ul>
			</div>
		</section>

		<section class="feature feature--share">
			<div class="info">
				<p class="title">
					<span class="text-bl">
						Teile
					</span>
					Reiserouten mit
					<br />
					anderen Backpackern
				</p>

				<img class="image image--mobile" alt="Teile Reiserouten mit anderen Backpackern" lazy src="@/assets/feature-c2.png" />

				<p class="sub-title">
					Lass dich von anderen Routen inspirieren und teile deine eigene Reiseerfahrung.
				</p>

				<ul class="list">
					<li>
						<img lazy alt="Check mark icon" src="@/assets/checkmark-icon.svg" width="15" />
						Buche Reiserouten von anderen Backpackern
					</li>
					<li>
						<img lazy alt="Check mark icon" src="@/assets/checkmark-icon.svg" width="15" />
						Lerne von ihren Bewertungen, Erfahrungen und Tipps
					</li>
					<li>
						<img lazy alt="Check mark icon" src="@/assets/checkmark-icon.svg" width="15" />
						Werde Travel Star und teile deine Reiserouten mit der Welt
					</li>
				</ul>
			</div>

			<div class="image">
                <img alt="Teile Reiserouten mit anderen Backpackern" lazy src="@/assets/feature-c2.png" />
			</div>
		</section>

		<section class="backpackers">
			<h2>
				Was Backpacker über uns sagen:
			</h2>

			<div class="items">
				<div class="item">
					<img lazy src="@/assets/hannah-avater.jpeg" alt="Hannah avatar" />
					<span class="name">
						Hannah
					</span>
					<p class="description">
						„Als Backpacker will ich nicht dahin, wo alle anderen auch hingehen. Hier aber kann ich Reiseziele finden, die genau zu mir passen.“
					</p>
				</div>
				<div class="item">
					<img lazy src="@/assets/luisa-avatar.jpeg" alt="Luisa avatar" />
					<span class="name">
						Luisa
					</span>
					<p class="description">
						„Die Webapp ist ein tolles Tool, um eigene Reisen zu dokumentieren und mit Familie und Freunden zu teilen.“
					</p>
				</div>
				<div class="item">
					<img lazy src="@/assets/jonas-avatar.jpeg" alt="Jonas avatar" />
					<span class="name">
						Jonas
					</span>
					<p class="description">
						„Es gibt nichts nervigeres, als Flüge und Unterkünfte herauszusuchen. Danke, dass ihr mir das abnehmt!“
					</p>
				</div>
			</div>
		</section>
    </div>
</template>

<script lang="ts">
  export default {
    name: 'TheLanding',
    data() {
      return {
        title: "Erstelle, teile und buche Backpacking Routen",
        description: "Tausche Travel-Storys und Reiserouten mit unserer Community aus und buche dein nächstes Abenteuer.",
        button: "Reise starten"
      }
    }
  }
</script>

<style scoped lang="scss">
    .container {
        .banner {
            align-items: center;
            background-image: url(@/assets/banner.jpg);
            background-position: center;
            background-repeat: no-repeat;
            background-size: cover;
            display: flex;
            height: 500px;
            justify-content: space-between;
            margin: 0;
            padding-top: var(--ui-navbar-height);
            padding-left: var(--ui-global-margin);
            padding-right: var(--ui-global-margin);
            position: relative;
            width: 100%;
            .content {
                align-items: flex-start;
                flex-direction: column;
                width: 65%;
                display: flex;
                h1,
                p {
                    color: #fff;
                }
                h1 {
                    font-size: 2.8rem;
                    font-weight: 700;
                    line-height: 2.8rem;
                    margin-bottom: 24px;
                }
                p {
                    font-size: 1.2rem;
                    font-weight: 400;
                    line-height: 1.5rem;
                    margin-bottom: 20px;
                }
                .start {
                    all: unset;
                    background: var(--ui-color-primary);
                    border-radius: 30px;
                    color: var(--ui-color-text);
                    cursor: pointer;
                    font-size: 1.2rem;
                    font-weight: 700;
                    line-height: 28px;
                    padding: 16px 4rem;
                    transition: background .2s linear .1s;
                }
            }
        }
        .trust {
            background: #fff;
            border-bottom: 2px solid #E5E5E5;
            padding: 2rem var(--ui-global-margin);
            h2 {
                color: #A5A5A5;
                font-weight: 400;
                font-size: 1.8rem;
                line-height: 24px;
                margin: 21px 0px;
            }
            .companies {
                align-items: center;
                display: flex;
                justify-content: space-around;
                padding-bottom: 2rem;
                img {
                    max-width: 11rem;
                    width: 13%;
                }
            }
        }
        .options {
            background: #fff;
            padding: 4rem var(--ui-global-margin);
            .title {
                color: #476572;
                font-size: 1.8rem;
                margin: 2rem auto;
                text-align: center;
            }
            .items {
                align-items: flex-end;
                display: flex;
                justify-content: space-around;
                .item {
                    text-align: center;
                    p {
                        color: #476572;
                        font-size: 1.4rem;
                        font-weight: 700;
                        margin-top: 1.5rem;
                    }
                }
            }
        }
        .solution {
            margin: 4rem auto;
            .title {
                color: var(--ui-color-primary);
                font-size: 1.8rem;
                text-align: center;
            }
        }
        .feature {
            align-items: center;
            display: flex;
            justify-content: space-between;
            width: 100%;
            & > div {
                width: 50%;
            }
            .text-bl {
                color: var(--ui-color-primary);
                display: inline-block;
            }
            .image {
                padding: 0 4rem;
                img {
                    margin: 0 auto;
                    width: 100%;
                }
                &--mobile {
                    display: none;
                }
            }
            .info {
                & > * {
                    font-weight: 400;
                }
                .title {
                    color: #476572;
                    font-size: 1.8rem;
                    line-height: 2rem;
                }
                .sub-title {
                    font-size: 1rem;
                    line-height: 1.2rem;;
                    margin: 2rem 0;
                }
                ul {
                    list-style-type: none;
                    padding: 0;
                    position: relative;
                    li {
                        color: #283C45;
                        font-size: .75rem;
                        img {
                            margin-right: 0.5rem;
                        }
                    }
                }
            }
            &--create {
                padding: 2rem var(--ui-global-margin);
                .info {
                    padding-left: 2rem;
                }
            }
            &--share {
                background: #F6F6F6;
                padding: 5rem var(--ui-global-margin);
                width: 100%;
            }
            &--share {
                .info {
                    padding-right: 2rem;
                }
            }
        }
        .backpackers {
            padding: 3rem var(--ui-global-margin);
            h2 {
                color: #476572;
                font-size: 1.8rem;
                font-weight: 400;
                margin-bottom: 2rem;
            }
            .items {
                display: flex;
                justify-content: space-between;
                padding-top: 5rem;
                .item {
                    background: #fff;
                    border-radius: 20px;
                    box-shadow: 0px 8px 24px rgba(0, 0, 0, 0.08);
                    display: flex;
                    flex-direction: column;
                    padding: 0 24px 24px;
                    text-align: left;
                    width: 30%;
                    > * {
                        margin-bottom: 1rem;
                    }
                    .name {
                        color: #283C45;
                        display: block;
                        font-size: 1.6rem;
                        font-weight: 700;
                        line-height: 1.6rem;
                        margin-top: 2rem;
                    }
                    .description {
                        color: #283C45;
                        font-size: 1rem;
                        font-weight: 400;
                        line-height: 1.6rem;
                    }
                    img {
                        border-radius: 8rem;
                        display: block;
                        height: 8rem;
                        margin: 0 auto;
                        margin-top: -4rem;
                        width: 8rem;
                    }
                }
            }
        }
    }

    @media all and (max-width: 477px) {
        .container {
            .banner {
                .content {
                    align-items: center;
                    text-align: center;
                    width: 100%;
                    h1 {
                        font-size: 2rem;
                        line-height: 2rem;
                    }
                    .start {
                        font-size: 1rem;
                        padding: 10px 2rem;
                    }
                }
            }
            .trust {
                border-bottom: 2px solid #E5E5E5;
                padding: 1.8rem var(--ui-global-margin) 1rem;
                h2 {
                    font-size: 1rem;
                    text-align: center;
                }
                .companies {
                    align-items: center;
                    display: flex;
                    flex-wrap: wrap;
                    justify-content: space-evenly;
                    padding-bottom: 2rem;
                    img {
                        margin-bottom: 1rem;
                        max-width: 35%;
                        width: 20rem;
                    }
                }
            }
            .options {
                padding: 4rem var(--ui-global-margin);
                .title {
                    font-size: 1.8rem;
                    text-align: center;
                }
                .items {
                    align-items: center;
                    flex-wrap: wrap;
                    .item {
                        &:not(:first-child) {
                            margin-top: 2rem;
                        }
                        p {
                            font-size: 1.2rem;
                            margin-top: 0;
                        }
                    }
                }
            }
            .feature {
                align-items: center;
                flex-direction: column;
                justify-content: center;
                & > div {
                    width: 100%;
                }
                .title {
                    text-align: center;
                    width: 100%;
                }
                .image {
                    display: none;
                    padding: 0;
                    &--mobile {
                        display: block;
                        margin: 2rem auto;
                        width: 100%;
                    }
                }
                .info {
                    padding: 0;
                    .title {
                        color: #476572;
                        font-size: 1.8rem;
                        line-height: 2rem;
                    }
                    .sub-title {
                        text-align: center;
                    }
                }
            }
            .backpackers {
                h2 {
                    text-align: center;
                }
                .items {
                    flex-direction: column;
                    justify-content: center;
                    .item {
                        text-align: center;
                        width: 100%;
                        &:not(:last-child) {
                            margin-bottom: 6rem;
                        }
                    }
                }
            }
        }
    }
</style>