# Get-Form-Data-with-JavaScript
get data from a FORM with JavaScript


// getting the Form element and listener it
document.querySelector('form')
    .addEventListener('submit', e => {
        // stop the default functions 
        e.preventDefault()
        // store the data in a variable, create new FormData to intruduce the form target data
        const data = Object.fromEntries(
            new FormData(e.target)
        )
        // show the Object in a console log
        console.log(JSON.stringify(data))
    })
