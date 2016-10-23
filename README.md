<head>
<style>
.thumbnail {
    -webkit-backface-visibility: hidden;
    display: inline-block;
    position: relative;
    margin: 0 auto;
    overflow: hidden;
    background: #000;
    box-shadow: 0 15px 50px rgba(0,0,0,.5);
}
.thumbnail img {
    display: block;
    max-width: 100%;
    transition: opacity .2s ease-in-out;
}
.thumbnail:hover img {
    opacity: .5;
}
.thumbnail::after,
.thumbnail::before {
    position: absolute;
    z-index: 1;
    width: 100%;
    height: 50%;
    transition: transform .4s ease-out;
    color: #fff;
}
.thumbnail::after {
    content: attr(data-title);
    top: 0;
    padding-top: 55px;
    transform: translateY(-100%) scale(.8);
    background: rgba(0,0,0,.4);
    font-size: 3.5rem;
    font-weight: 300;
    font-family: Merriweather, serif;
    text-align: center;
}
.thumbnail::before {
    content: attr(data-description) "…";
    top: 50%;
    padding: 20px;
    transform: translateY(100%) scale(.8);
    background: rgba(107,38,68,.6);
    -webkit-backdrop-filter: blur(10px);
    backdrop-filter: blur(10px);
    color: #f1f1f1;
    font-size: 1.5rem;
}
.thumbnail:hover::after,
.thumbnail:hover::before {
    transform: translateY(0%) scale(1);
}
</style>
</head>
<body>  
  <main>
        <section id="container">
            <div class="thumbnail"
                data-title="Bacon"
                data-description="Bacon ipsum dolor amet filet mignon alcatra short ribs, sausage shoulder tail biltong rump chicken ground round ham hock porchetta tri-tip. Boudin bresaola andouille, leberkas pork ball tip turducken beef ribs">
                <img src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/123941/meat.jpg" alt="Meat" width="300">
            </div>
        </section>
    </main>
</body>
