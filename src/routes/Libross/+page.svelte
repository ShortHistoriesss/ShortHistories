
<script>
    import Logo from './Logo_sin_fondo.png';
    let searchQuery = '';
    let items = [ 
        { 
            title: 'Meter el diablo en el infierno', 
            author: 'Giovanni Boccaccio', 
            image: 'https://www.booktopia.com.au/covers/big/9781413517118/0000/meter-el-diablo-en-el-infierno.jpg', 
            link: '/meter_el_diablo_en_el_infierno.pdf' 
        }, 
        { 
            title: 'El cocinero chichibio', 
            author: 'Giovanni Boccaccio', 
            image: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRF9TPWlnMe24ZMpUSzhkDN6_vmlngGrILMIQ&s.jpg', 
            link: '/El-cocinero-Chichibio.pdf' 
        }, 
        { 
            title: 'Historias de las Historias', 
            author: 'Carlos Fisas', 
            image: 'https://www.planetadelibros.com.co/usuaris/libros/fotos/55/m_libros/54157_historias-de-la-historia_9788408101864.jpg', 
            link: '/Historias-de-a-Historia.pdf' 
        }, 
        { 
            title: 'Las mil y una noche', 
            author: 'Carlos Fisas', 
            image: 'https://images.cdn2.buscalibre.com/fit-in/360x360/b9/4d/b94d245d5ee98477b44f09cfd7e58c13.jpg', 
            link: '/Las-mil-y-una-noches.pdf' 
        }, 
        { 
            title: 'Historias de noche', 
            author: 'J.A WHITE', 
            image: 'https://http2.mlstatic.com/D_NQ_NP_972412-MLA50115243457_052022-O.webp.jpg', 
            link: '/47796_Historia_de_noche.pdf' 
        }, 
        { 
            title: 'La luz del faro', 
            author: 'Vicente Muñoz Puelles', 
            image: 'https://images.cdn1.buscalibre.com/fit-in/360x360/fe/5d/fe5df6fbd58f6af99788645240e381d4.jpg', 
            link: '/Luz-de-faro.pdf' 
        }, 
        { 
            title: 'El retrato oval', 
            author: 'Edgar Allan Poe', 
            image: 'https://covers.libro.fm/9798882264764_1120.jpg', 
            link: '/El_retrato_oval-Allan_Poe_Edgar.pdf' 
        }, 
        { 
            title: 'La metamorfosis', 
            author: 'Franz Kafka', 
            image: 'https://www.agapea.com/poltada-i6n15704524.jpg', 
            link: '/Lametamorfosis.pdf' 
        },
        { 
            title: 'El extranjero', 
            author: 'Albert Camus', 
            image: 'https://th.bing.com/th/id/OIP.xqWKeFTnOt3s00o7bCBxRAHaLC?rs=1&pid=ImgDetMain', 
            link: 'elextranjero.pdf' 
        },
        { 
            title: 'La perla', 
            author: 'John Steinbeck', 
            image: 'https://horadelrecreo.com/wp-content/uploads/2020/03/LIBRO-LA-PERLA3-e1583232858885.jpg', 
            link: 'laperla.pdf' 
        },
        { 
            title: 'El principito', 
            author: 'Antoine de Saint-Exupéry', 
            image: 'https://th.bing.com/th/id/R.e5d6c1e5331d5cdd40bd14932c62b296?rik=uj6%2f%2foMh8Kz5PA&pid=ImgRaw&r=0', 
            link: 'elprincipito.pdf' 
        },
        { 
            title: 'El viejo y el mar', 
            author: 'Ernest Hemingway', 
            image: 'https://3.bp.blogspot.com/-HfkJQCUI1DY/Vd5TnzI7OJI/AAAAAAAABvQ/chr71p8NZiI/s1600/el-viejo-y-el-mar.jpg', 
            link: 'El Viejo y El Mar.PDF' 
        },
        { 
            title: 'La nariz', 
            author: 'Nikolai Gogol', 
            image: 'https://th.bing.com/th/id/OIP.eJg7Xv5QD4_bwW2kQdrV4wAAAA?rs=1&pid=ImgDetMain', 
            link: 'Lanariz.pdf' 
        },
        { 
            title: 'Aura', 
            author: 'Carlos Fuentes', 
            image: 'https://th.bing.com/th/id/OIP.b0eipjuboqRUgH6ymTqkYwAAAA?rs=1&pid=ImgDetMain', 
            link: 'aura.pdf' 
        },
        { 
            title: 'La tregua', 
            author: 'Mario Benedetti', 
            image: 'https://th.bing.com/th/id/R.eb7c4d3d2c0a8c743f7259efe63b9781?rik=GptLvmzQnmrj2g&pid=ImgRaw&r=0', 
            link: 'latregua.pdf' 
        },
        { 
            title: 'A Christmas Carol', 
            author: 'Charles Dickens', 
            image: 'https://th.bing.com/th/id/R.1cba694468a232d696a312ed4176c3c3?rik=vYBfZZoh4U7M7A&pid=ImgRaw&r=0', 
            link: 'Chrismas.pdf' 
        },
        { 
            title: 'Siddhartha', 
            author: 'Hermann Hesse', 
            image: 'https://th.bing.com/th/id/R.57022accd78aeca0932869697afd3c84?rik=EEmGTEFei8hmuQ&pid=ImgRaw&r=0', 
            link: 'Siddhartha.pdf' 
        },
        { 
            title: 'Frankenstein', 
            author: 'Mary Shelley', 
            image: 'https://th.bing.com/th/id/OIP.l6PbFg5hJTuNbgu-jgi5RAHaLc?rs=1&pid=ImgDetMain', 
            link: 'Franks.pdf' 
        },
        { 
            title: 'Breakfast at Tiffanys', 
            author: 'Truman Capote', 
            image: 'https://th.bing.com/th/id/OIP.7iL5as7b05uQZGmdCAPk5QAAAA?rs=1&pid=ImgDetMain', 
            link: 'Breakfast.pdf' 
        },
        { 
            title: 'The House on Mango Street', 
            author: 'Sandra Cisneros', 
            image: 'https://cdn.slidesharecdn.com/ss_thumbnails/0679734775-thehouseonmangostreetbysandracisneros-181105161326-thumbnail-4.jpg?cb=1541434445', 
            link: 'Mangostreet.pdf' 
        },
        { 
            title: 'The Lottery', 
            author: 'Shirley Jackson', 
            image: 'https://th.bing.com/th/id/OIP.-VMslK9sirncwWST0C6spwHaKg?rs=1&pid=ImgDetMain', 
            link: 'lottery.pdf' 
        },
        { 
            title: 'The Little Prince', 
            author: 'Antoine de Saint-Exupéry', 
            image: 'https://imagessl1.casadellibro.com/a/l/t0/11/9783965448711.jpg', 
            link: 'ThePrince.pdf' 
        },
        { 
            title: 'The Giver', 
            author: 'Lois Lowry', 
            image: 'https://cdn11.bigcommerce.com/s-gibnfyxosi/images/stencil/2560w/products/172091/173708/41UGoSAEkKL__54825.1615625836.jpg?c=1', 
            link: 'The Giver.pdf' 
        },
        { 
            title: 'Coraline', 
            author: 'Neil Gaiman', 
            image: 'https://th.bing.com/th/id/OIP.fJTbPSbzW3LQexwKiljZMwAAAA?rs=1&pid=ImgDetMain', 
            link: 'coraline.pdf' 
        },
        { 
            title: 'The War of the Worlds', 
            author: 'H.G. Wells', 
            image: 'https://th.bing.com/th/id/OIP.rLF2r6tLSFNJ1ZxrMj_s6wAAAA?rs=1&pid=ImgDetMain', 
            link: 'Warofworlds.pdf' 
        },
        { 
            title: 'Animal Farm', 
            author: 'George Orwell', 
            image: 'https://th.bing.com/th/id/R.86b7dd2623658b5113f3602b3196a752?rik=Ox0xfOfNTQfU6g&pid=ImgRaw&r=0', 
            link: 'animalfarm.pdf' 
        },
        { 
            title: 'Charlottes Web', 
            author: 'E.B. White', 
            image: 'https://th.bing.com/th/id/OIP.Kgn-5cc9dDGvajcGsrYPhwAAAA?rs=1&pid=ImgDetMain', 
            link: 'Charlotte.pdf' 
        },
        { 
            title: 'The Tale of Peter Rabbit ', 
            author: 'Beatrix Potter', 
            image: 'https://www.familyandhomeliving.com/wp-content/uploads/2022/03/the-tale-of-peter-rabbit-pdf-768x576.jpg', 
            link: 'PeterRabbit.pdf' 
        },
        { 
            title: 'Flatland: A Romance of Many Dimensions', 
            author: 'Edwin A. Abbott', 
            image: 'https://th.bing.com/th/id/OIP.m42d6OmP4UUgTiBbYnSCZwAAAA?rs=1&pid=ImgDetMain', 
            link: 'flatland.pdf' 
        },
        { 
            title: 'The Curious Case of Benjamin Button', 
            author: 'F. Scott Fitzgerald', 
            image: 'https://th.bing.com/th/id/OIP.9mXrFIaJWC0UAxeRS7p4nAHaLp?rs=1&pid=ImgDetMain', 
            link: 'The Curious Case.pdf' 
        },
        { 
            title: 'The Little Match Girl', 
            author: 'Hans Christian Andersen', 
            image: 'https://th.bing.com/th/id/R.60e499721124a9bdedb6293b77284603?rik=W9L9kl%2fWmB3Cww&pid=ImgRaw&r=0', 
            link: 'littlematchgirl.pdf' 
        },
        { 
            title: 'Manual para mujeres de la limpieza', 
            author: 'Lucia Berlin', 
            image: 'https://th.bing.com/th/id/R.d621807f7adcbaa2c0914c640ada9185?rik=j99U6NKpttBqvQ&pid=ImgRaw&r=0', 
            link: 'manuelmujeres.pdf' 
        },
        { 
            title: 'Casa de muñecas', 
            author: 'Patricia Esteban Erlés', 
            image: 'https://th.bing.com/th/id/R.3b21ce403339f21973e82d1ea691b9af?rik=A6YlNGL6JaE78Q&riu=http%3a%2f%2flapiedradesisifo.com%2fwp-content%2fuploads%2f2014%2f06%2f44990.jpg&ehk=wfKJ%2fZXSeQmhTBfY%2f4hDnrMphzu8CbL11YZcHnM3nXg%3d&risl=&pid=ImgRaw&r=0', 
            link: 'muñecas.pdf' 
        },
        { 
            title: 'Las cosas que perdimos en el fuego', 
            author: 'Mariana Enríquez', 
            image: 'https://th.bing.com/th/id/OIP.aN9t_MNwnP_tSdUk77PsNAHaLo?rs=1&pid=ImgDetMain', 
            link: 'lascosasqueperdimos.pdf' 
        },
        { 
            title: 'Voces de Chernóbil', 
            author: 'Svetlana Alexievich', 
            image: 'https://th.bing.com/th/id/OIP.2D5U4cobXncPt_r7Dw0lggHaLQ?rs=1&pid=ImgDetMain', 
            link: 'voceschernobil.pdf' 
        },
        { 
            title: 'Historias de cronopios y de famas', 
            author: 'Julio Cortázar', 
            image: 'https://th.bing.com/th/id/R.9e902f94a54b3424ee8c23b201cc6c88?rik=OP61HfGlr1cMPA&pid=ImgRaw&r=0', 
            link: 'Historiafamas.pdf' 
        },
        { 
            title: 'El Aleph', 
            author: 'Jorge Luis Borges', 
            image: 'https://th.bing.com/th/id/OIP.bbIStDykoWaPZPhWr9thxgAAAA?rs=1&pid=ImgDetMain', 
            link: 'Elaleph.pdf' 
        },
        { 
            title: 'Los girasoles ciegos', 
            author: 'Alberto Méndez', 
            image: 'https://th.bing.com/th/id/R.7503b2adc34b324a92af43bff15a0555?rik=rzHqzhmRuSxU1A&pid=ImgRaw&r=0', 
            link: 'losgirasoles.pdf' 
        },
        { 
            title: 'El libro de los abrazos', 
            author: 'Eduardo Galeano', 
            image: 'https://th.bing.com/th/id/OIP.GPBupsFTJFA85ZAS-twqJgHaLf?rs=1&pid=ImgDetMain', 
            link: 'abrazos.pdf' 
        }
        
    ];
    let filteredItems = items; 
    function handleSearch() { 
        filteredItems = items.filter(item => item.title.toLowerCase().includes(searchQuery.toLowerCase()));
        filteredItems = items.filter(item => item.author.toLowerCase().includes(searchQuery.toLowerCase())); 
    };
</script>

<svelte:head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Libros</title>
    <link rel="shortcut icon" href={Logo} type="image/x-icon">

    <style>
    *{
    margin: 0;
    padding: 0;
    text-decoration: none;
    border: none;
    outline: none;
    font-family: 'Poppins', sans-serif;
    }

    body{
    font-size: 62.5%;
        width: 100%;
        height: 100vh;
        overflow-x: hidden;
        background-color: black;
        color: white;
    }

    </style>
</svelte:head>
  

<div class="all">
    <div class="header">
        <p  class="logo"> <a href="./"> <img src={Logo} height="60px" width="60" alt="" /> </a>  </p>
        <div class="search-container">
            <input type="text" bind:value={searchQuery} on:input={handleSearch} class="search-box" placeholder="Buscar...">
            <button on:click={handleSearch} class="btnb">Buscar</button>
        </div>
        <nav class="active">
            <a href="/Escribe">Comienza a escribir</a>
            <a href="#final">Redes sociales</a>
            <a href="."> aa</a>
        </nav>
    </div>

    <section>
        <div class="container">
            {#each filteredItems as item} 
                <div class="card"> 
                    <div class="image-container"> 
                        <img src={item.image} alt={item.title}> 
                    </div> 
                    <div class="card-content"> 
                        <h1 class="card-title"><span>{item.title}</span></h1> 
                        <p class="card-description">{item.author}</p> 
                        <a href={item.link} target="_blank"> 
                            <button class="btn">Leer más</button> 
                        </a> 
                    </div> 
                </div> 
                
                
            {/each}
        </div>
    </section>

	<section id="final">
			<h2>Si gustas puedes seguirnos en nuestras redes sociales </h2>
			<div class="social-icons">
				<a href="https://x.com/ShortHistoriess"><i class="fa-brands fa-x-twitter"></i></a>
				<a href="https://www.instagram.com/short_historiess/"><i class="fa-brands fa-instagram"></i></a>
                <a href="https://www.tiktok.com/@shorthistoriess0?lang=es"><i class="fa-brands fa-tiktok"></i></a>
			</div>
	</section>
</div>

<style>
	

    .logo {
		font-size: 25px;
		color: #b74b4b;
		font-weight: 800;
		cursor: pointer;
		transition: 0.5s ease;
	}

	.logo:hover {
		transform: scale(1.1);
	}

    .search-container {
        display: flex;
        justify-content: center;
        
    }
    .search-box {
        width: 300px;
        padding: 10px;
        border: 1px solid #ccc;
        border-radius: 4rem;
    }

    .btnb {
		display: inline-block;
		padding: 0.7rem 2rem;
		background-color: black;
		border-radius: 4rem;
		font-size: 15px;
		color: #b74b4b;
		font-weight: 600;
		border: 2px solid #b74b4b;
		transition: 0.3s ease;
		cursor: pointer;
	}

	.btnb:hover {
		transform: scale3d(1.03);
		background-color: #b74b4b;
		color: black;
		box-shadow: 0 0 25px #b74b4b;
	}

    

	span {
		color: #b74b4b;
	}

    .container {
        display: grid;
        grid-template-columns: repeat(3, 1fr); /* Dos columnas */
        gap: 20px; /* Espacio entre tarjetas */
        justify-content: center;
        margin-top: 100px;
        padding: 20px;
    }

    .card {
        background-color: #000000;
        color: #ffffff;
        padding: 20px;
        border-radius: 5px;
        box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
        display: flex;
        align-items: center;
        gap: 20px;
    }

    .image-container img{
        width: 150px;
        height: 200px;
        background-color: #ddd;
        border: 2px solid #ffffff;
        border-radius: 5px;
        border-color: #b74b4b;
        border-width: 2%;
    }

    .card-content {
        display: flex;
        flex-direction: column;
    }

    .card-title {
        font-size: 24px;
        font-weight: bold;
        margin-bottom: 10px;
    }

    .card-description {
        font-size: 16px;
        line-height: 1.5;
        margin-bottom: 20px;
    }

    
	.btn {
		display: inline-block;
		padding: 1rem 2.8rem;
		background-color: black;
		border-radius: 4rem;
		font-size: 1rem;
		color: #b74b4b;
		font-weight: 600;
		border: 2px solid #b74b4b;
		transition: 0.3s ease;
		cursor: pointer;
	}

	.btn:hover {
		transform: scale3d(1.03);
		background-color: #b74b4b;
		color: black;
		box-shadow: 0 0 25px #b74b4b;
	}

    .header {
		margin-top: 20px;
		position: fixed;
		top: 0;
		left: 0;
		width: 100%;
		padding: 1rem 4%;
		background-color: rgba(0, 0, 0, 0);
		filter: drop-shadow(10px);
		display: flex;
		justify-content: space-between;
		align-items: center;
		z-index: 100;
	}

    
	nav a {
		font-size: 20px;
		color: white;
		margin-left: 4rem;
		font-weight: 500;
		transition: 0.3s ease;
		border-bottom: 3px solid transparent;
	}

	nav a:hover,
	nav a.active {
		color: #b74b4b;
		border-bottom: 3px solid #b74b4b;
	}

	@media (max-width: 995px) {
		nav {
			position: absolute;
			display: none;
			top: 0;
			right: 0;
			width: 40%;
			border-left: 3px solid #b74b4b;
			border-bottom: 3px solid #b74b4b;
			border-bottom-left-radius: 2rem;
			padding: 1rem solid;
			background-color: #161616;
			border-top: 0.1rem solid rgba(0, 0, 0, 0.1);
		}

		nav.active {
			display: block;
		}

		nav a {
			display: block;
			font-size: 15px;
			margin: 3rem 0;
		}

		nav a:hover,
		nav a.active {
			padding: 1rem;
			border-radius: 0.5rem;
			border-bottom: 0.5rem solid #b74b4b;
		}

    }
	
    #final {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		text-align: center;
        padding: 50px;
		background-color: rgb(30, 30, 30);
		background-image: linear-gradient(0deg, rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), url('a.jpg');
		background-repeat: no-repeat;
		background-size: 1500px;
		color: white;
		height: 90vh;
	}

	#final h2 {
		font-size: 45px;
	}

	#final button {
		font-size: 20px;
	}

    
	.social-icons a {
		display: inline-flex;
		justify-content: center;
		align-items: center;
		width: 4rem;
		height: 4rem;
		background-color: transparent;
		border: 0.2rem solid #b74b4b;
		font-size: 2rem;
		border-radius: 50%;
		margin: 3rem 1.5rem 3rem 0;
		transition: 0.3s ease;
		color: #b74b4b;
	}

	.social-icons a:hover {
		color: black;
		transform: scale(1.3) translateY(-5px);
		background-color: #b74b4b;
		box-shadow: 0 0 25px #b74b4b;
	}
	
</style>