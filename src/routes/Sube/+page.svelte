
<script>
    import Logo from './Logo_sin_fondo.png';
	let pdfs = [];
    let pdfName = '';
    let selectedFile = null;
    let pdfUrl = '';
  
    const addPdf = () => {
      if (pdfName && selectedFile) {
        pdfUrl = URL.createObjectURL(selectedFile);
        pdfs = [...pdfs, { name: pdfName, url: pdfUrl }];
        pdfName = '';
        selectedFile = null;
        document.getElementById('fileInput').value = '';  // reset file input
      }
    };
  
    const removePdf = (index) => {
      pdfs = pdfs.filter((_, i) => i !== index);
    };
  
    const handleFileChange = (event) => {
      selectedFile = event.target.files[0];
    };
    
</script>

<svelte:head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Sube tu historia</title>
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
        <p  class="logo"> <a href="./Escribe"> <img src={Logo} height="60px" width="60" alt="" /> </a>  </p>
        <nav class="active">
            <a href="#final">Redes sociales</a>
            <a href=""> aa</a>
        </nav>
    </div>

	<div class="r"> 
		<section> 
			<div class="container"> 
				<div class="input-field"> 
					<input type="text" bind:value={pdfName} placeholder="Nombre del PDF" /> 
				</div> 
				<br>
				<div class="file-input-container"> 
					<label for="fileInput" class="file-input-label">Seleccionar PDF</label> 
					<input type="file" accept="application/pdf" id="fileInput" class="file-input" on:change={handleFileChange} /> 
					<button class="btnb" on:click={addPdf}>Agregar PDF</button> 
				</div>
				
				<div class="pdf-list"> 
					{#each pdfs as pdf, index} 
						<div class="pdf-item"> 
							<a href={pdf.url} target="_blank" class="pdf-name">{pdf.name}</a> 
							<button class="btnb" on:click={() => removePdf(index)}>Eliminar</button> 
						</div> 
					{/each} 
				</div>
			</div>
    	</section>
	</div>
    

	<section id="final">
			<h2>Si gustas puedes seguirnos en nuestras redes sociales </h2>
			<div class="social-icons">
				<a href="https://x.com/ShortHistoriess"><i class="fa-brands fa-x-twitter"></i></a>
				<a href="https://www.instagram.com/short_historiess/"><i class="fa-brands fa-instagram"></i></a>
                <a href="https://www.tiktok.com/@shorthistoriess0?lang=es"><i class="fa-brands fa-tiktok"></i></a>
			</div>
	</section>


<style>

	.r {
		display: flex; 
		justify-content: center; 
		align-items: center; 
		height: 100vh; 
		margin: 0; 
		background-color: black; 
		color: white;
	}
	.file-input-container { 
		display: flex; justify-content: center; 
		align-items: center; 
		flex-direction: row; 
		margin-top: 20px; 
	} 
	
	.file-input-label { 
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
		margin-right: 10px; /* Espacio entre los botones */ 
	} 
	
	.file-input-label:hover { 
		transform: scale(1.03); 
		background-color: #b74b4b; 
		color: black; 
		box-shadow: 0 0 25px #b74b4b; 
	} 
	
	.file-input { 
		display: none; 
	} 

	.input-field { 
		max-width: 380px; 
		width: 100%; 
		background-color: #f0f0f0; 
		margin: 10px 0; 
		height: 55px; 
		border-radius: 55px; 
		display: flex; 
		align-items: center; 
		padding: 0 1rem; 
		border: 2px solid #b74b4b; 
	} 
	
	.input-field input { 
		background: none; 
		outline: none; 
		border: none; 
		width: 100%; 
		height: 100%; 
		line-height: 1; 
		font-weight: 600; 
		font-size: 1.1rem; 
		color: #333; 
		padding: 0 1rem; 
	} 
	
	.input-field input::placeholder { 
		color: #aaa; 
		font-weight: 500; 
	} 

	.pdf-list { 
		display: flex; 
		flex-direction: column; 
		align-items: center; 
		margin-top: 20px; 
	} 
	
	.pdf-item { 
		display: flex; 
		justify-content: space-between; 
		align-items: center; 
		width: 100%; 
		background-color: #f0f0f0; 
		padding: 10px;
		margin: 10px 0; 
		border-radius: 10px; 
		border: 2px solid #b74b4b; 
	} 
	
	.pdf-name { 
		color: #333; 
		font-weight: 600; 
		text-decoration: none; 
		font-size: 18px; 
		margin-right: 10px; 
	} 
	
	.pdf-name:hover { 
		text-decoration: underline; 
		color: #b74b4b; 
	} 
	
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