<template>
    <div class="container">
        <section class="banner">
            <div class="content">
                <h1>{{ title }}</h1>
                <p>{{ description }}</p>
            </div>
        </section>

		<section class="feature feature--create">
			<div class="image image--desktop">
				<img alt="Sich selbst kennenlernen" lazy src="@/assets/about-c1.jpg" />
			</div>

			<div class="info">
				<p class="title">
                    Sich
                    <br />
                    selbst
					<span class="text-bl">
						kennenlernen
					</span>
				</p>

				<img class="image image--mobile" alt="Sich selbst kennenlernen" lazy src="@/assets/about-c1.jpg" />

				<p class="sub-title">
					Reisen erweitert den Horizont. Nicht nur bezüglich der Welt dort draußen, sondern auch bezüglich einem selbst. Was treibt dich an?
					<br />
					Was gibt dir Kraft? Was beflügelt dich, um deine Komfortzone zu verlassen und als Mensch zu wachsen? Gehe hinaus in die Welt und finde es heraus.
				</p>
			</div>
		</section>

		<section class="feature feature--share">
			<div class="info">
				<p class="title">
                    Andere
					<span class="text-bl">
						kennenlernen
					</span>
				</p>

				<img class="image image--mobile" alt="Andere kennenlernen" lazy src="@/assets/about-c2.jpg" />

				<p class="sub-title">
					Die Erde ist groß und bunt und so sind ihre Bewohner. Vielleicht triffst du Reisende, die dich einen Schritt begleiten, nur weil sich eure Wege kreuzen.
                    <br />
                    Oder du triffst Locals, die dir Land und Kultur näherbringen können. Suche aktiv nach dem Kontakt zu Anderen und du wirst schnell Freunde auf der ganzen Welt haben.
				</p>
			</div>

			<div class="image">
                <img alt="Andere kennenlernen" lazy src="@/assets/about-c2.jpg" />
			</div>
		</section>

    </div>
</template>

<script lang="ts">
  export default {
    name: 'TheLanding',
    data() {
      return {
        title: "Willkommen im Tribe!",
        description: "Unser außergewöhnlicher Tribe besteht aus mehr als 20 Nationen, die alle eine Leidenschaft teilen: das Backpacking. Als Teil des Tribes arbeitest du nicht für uns, sondern mit uns!",
      }
    }
  }
</script>

<style scoped lang="scss">
    .container {
        .banner {
            align-items: center;
            background-image: url(@/assets/about-banner.png);
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
        }
    }
</style>