# Desarrollo basado en pruebas

## 1 Ejecutar las pruebas de alguno de los proyectos anteriores

He ejecutado los tests de mi [proyecto de la asignatura](https://github.com/jcpulido97/ProyectoIV) como se puede ver a continuación

```bash
vagrant@vagrant:/vagrant/ProyectoIV$ pytest test/VMtest.py test/APItest.py
============================= test session starts ==============================
platform linux -- Python 3.6.5, pytest-3.8.2, py-1.6.0, pluggy-0.7.1
rootdir: /vagrant/ProyectoIV, inifile:
collected 20 items

test/VMtest.py ..........                                                [ 76%]
test/APItest.py ...                                                      [100%]

========================== 13 passed in 4.19 seconds ===========================
```



## 2 Para la aplicación que se está haciendo, escribir una serie de aserciones y probar que efectivamente no fallan. Añadir tests para una nueva funcionalidad.

```python
import unittest
from src.vm_test import VM

class TestVM(unittest.TestCase):
    def setUp(self):
        self.vm = VM()

    def test_ip(self):
        new_ip="0.0.0.0"
        self.assertTrue(self.vm.setIP(new_ip), 'Fallo en el cambio de ip')
        self.assertEqual(self.vm.getIP(), new_ip, 'Fallo en el cambio de ip')
        bad_formated_ip = "4561.16358.10.-12"
        self.assertFalse(self.vm.setIP(bad_formated_ip), 'Fallo, aceptó una ip mal formateada '+bad_formated_ip)
        self.assertFalse(self.vm.setIP("256.256.256.256"), 'Fallo, aceptó una ip imposible')
        self.assertEqual(self.vm.getIP(), new_ip, 'Fallo en el cambio de ip')

if __name__ == '__main__':
    unittest.main()
```

## 3 Crear algún conjunto de scripts de tests, usando tu lenguaje favorito, y ejecutarlos desde el marco de test más adecuado (o el que más te guste) para ese lenguaje.

Se han creado los siguientes tests para probar el microservicio.

1. [APItest.py](https://github.com/jcpulido97/ProyectoIV/blob/master/test/APItest.py)
2. [VMtest.py](https://raw.githubusercontent.com/jcpulido97/ProyectoIV/master/test/VMtest.py)

## 4 Instalar alguno de los entornos virtuales de `node.js` (o de cualquier otro lenguaje con el que se esté familiarizado) y, con ellos, instalar la última versión existente, la versión `minor` más actual de la 4.x y lo mismo para la 0.11 o alguna impar (de desarrollo).

En este caso he instalado [virtualenv](https://virtualenv.pypa.io/en/latest/) que es el encargado de crear entornos virtuales en python.

```bash
# Debian o Ubuntu
$ sudo apt-get install python-virtualenv virtualenv
```

