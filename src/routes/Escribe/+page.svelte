
<script>
    import Logo from './Logo_sin_fondo.png';
    import jsPDF from 'jspdf';
  
  let text = '';

  const downloadPDF = () => {
    const doc = new jsPDF();
    doc.text(text, 10, 10);
    doc.save('document.pdf');
  };
</script>

<svelte:head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Crea y escribe</title>
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


    <div class="header">
        <p  class="logo"> <a href="./Libross"> <img src={Logo} height="60px" width="60" alt="" /> </a>  </p>
        <nav class="active">
            <a href="./Sube">Sube tu historia</a>
            <a href="#final">Redes sociales</a>
            <a href=""> aa</a>
        </nav>
    </div>

    <section>
        <div class="container">
            <h2><span> Comienza</span> </h2>
            <textarea bind:value={text}></textarea>
            <button on:click={downloadPDF} class="btnb">Guardar</button>
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


<style>

	.container { 
		display: flex; 
		flex-direction: column; 
		justify-content: flex-end; 
		align-items: center; 
		
		padding: 120px 15px; 
		background-repeat: no-repeat; 
		background-size: cover; 
		background-position: center center; 
		max-width: 600px; 
		margin: 0 auto; 
		font-family: Arial, sans-serif; 
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
		transform: scale(1.03); 
		background-color: #b74b4b; 
		color: black; 
		box-shadow: 0 0 25px #b74b4b; 
	}

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


    textarea {
      width: 100%;
      height: 200px;
      margin-bottom: 10px;
	  border-radius: 2rem;
	  border: 4px solid #b74b4b;
    }

    h2 {
		font-size: 45px;
        text-align: center;
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