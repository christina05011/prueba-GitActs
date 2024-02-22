[![Automated API tests using Postman CLI](https://github.com/christina05011/prueba-GitActs/actions/workflows/testpostman.yml/badge.svg)](https://github.com/christina05011/prueba-GitActs/actions/workflows/testpostman.yml)

This is my first test with Git Actions!!
This is automatization!

# Changes in Postman test:

//Pruebas de estrés con bucle for (pruebas consecutivas).

for (var i = 0; i < 100; i++) {

    pm.test("A name is returned", () => {
        pm.expect(pm.response.json()).to.have.property('name');
        pm.expect(pm.response.json().name).to.be.a('string');
    })

    // Pruebas de rendimiento.

    pm.test("Status code is 200", function () {
        pm.response.to.have.status(200);
    });

    pm.test("Response time is less than 1000ms", function(){
        pm.expect(pm.response.responseTime).to.be.below(1000);
    });
}

// Pruebas de carga: cambiar el número de iteraciones.

Se modifica el número de iteraciones.
Se modifica el número de delay, que es el tiempo de espera de una iteración (consulta) a otra.

## Para ejecutar varios runners en paralelo (¡mismo tiempo!)

strategy:
      matrix:
        parallel:  # Number of jobs parallel, different runners execution.
          - 1
          - 2
          - 3
