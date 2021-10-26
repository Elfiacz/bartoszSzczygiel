<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <form action= "">
        <input type="text" name="pole" />
        <button type="submit">Pokaz</button>
    </form>
    <div class="wynik"></div>
    <script>

        //odwołujemy sie do formularzu, pobiramy ten formularz

        const formularz = document.querySelector('form');

        const div=document.querySelector('.wynik');

        //przypisujemy zdarzenie do naszego formulara, które uruchomi funkcje przez przeglądarke zdarzenie nazywa sie submit
        formularz.addEventListener ('submit', (e)=> {
            
            e.preventDefault();

            //odwolujemy sie do pola w formularzu i pobieramy jego wartosc
            const wartoscPolaFormularza = document.querySelector('input[name=pole]').value;
            
            if(wartoscPolaFormularza % 2 == 0){
                div.textContent='Liczba jest parzysta';
            } else {
                div.textContent='Liczba jest nie przysta';
            }
            
            
            //wartosc pola formularza wrzucamy do diva
            //div.textContent=wartoscPolaFormularza;

        } );
    </script>
    

    </form>
</body>
</html>
