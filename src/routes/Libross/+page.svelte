
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

    ]; 
    let filteredItems = items; 
    function handleSearch() { 
        filteredItems = items.filter(item => item.title.toLowerCase().includes(searchQuery.toLowerCase())); 
    }
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
            <a href="#final">Redes sociales</a>
            <a href=""> aa</a>
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