# Introducción: Concepto y soporte físico

## 1 Consultar en el catálogo de alguna tienda de informática el precio de un ordenador tipo servidor y calcular su coste de amortización a cuatro y siete años. Consultar [este artículo en Infoautónomos sobre el tema](http://infoautonomos.eleconomista.es/consultas-a-la-comunidad/988/).

Encontramos la siguiente [tabla de amortización](https://www.agenciatributaria.es/AEAT.internet/Inicio/Ayuda/Manuales__Folletos_y_Videos/Manuales_practicos/_Ayuda_Folleto_Actividades_economicas/3__Impuesto_sobre_la_Renta_de_las_Personas_Fisicas/3_5_Estimacion_directa_simplificada/3_5_4__Tabla_de_amortizacion_simplificada/3_5_4__Tabla_de_amortizacion_simplificada.html) de la Agencia Tributaria, el coeficiente lineal máximo de amortización anual es del 26%, y el máximo de años es de 10. La amortización se hace sobre la base imponible.

Caso de ejemplo:

	IBM x3650 m2 Intel Xeon 8 cores/32GB DDR3
	
	Precio: 860€
	
	Sin iva: 679.4€



Primer supuesto: Amortización a 4 años (25% anual).

| Año  | Acumulado | Restantes |
| :--: | :-------: | :-------: |
|  1   |  169.85   |  509.55   |
|  2   |   339.7   |   339.7   |
|  3   |  509.55   |  169.85   |
|  4   |   679.4   |     0     |



Segundo supuesto: Amortización a 7 años (14,29% anual).

| Año  | Acumulados | Restantes |
| :--: | :--------: | :-------: |
|  1   |   97.08    |  582.31   |
|  2   |   194.17   |  485.22   |
|  3   |   291.25   |  388.14   |
|  4   |   388.34   |  291.05   |
|  5   |   485.43   |  193.96   |
|  6   |   582.51   |   96.88   |
|  7   |   679.4    |     0     |



## 2. Comparar el coste durante un año de un ordenador con un procesador estándar y con el resto de las características similares en el caso de que la infraestructura comprada se usa solo el 1% o el 10% del tiempo.

Ambos VPS ofrecen el mismo procesador, misma ram y misma configuración de disco.

### VPS en OVH

- Coste de configuración: 0€
- Coste/mes: 94,99€

Total: 1139,88€



### VPS en DigitalOcean

- Coste de configuración: **$0**
- Coste/mes: **$160**

Total: $1920 ~ 1684,87€

## 3 Flags de cpuinfo

### Portatil

```
processor   : 0
vendor_id   : GenuineIntel
cpu family  : 6
model       : 69
model name  : Intel(R) Core(TM) i7-4500U CPU @ 1.80GHz
stepping    : 1
microcode   : 0x17
cpu MHz     : 774.000
cache size  : 4096 KB
physical id : 0
siblings    : 4
core id     : 0
cpu cores   : 2
apicid      : 0
initial apicid  : 0
fpu     : yes
fpu_exception   : yes
cpuid level : 13
wp      : yes
flags       : fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush dts acpi mmx fxsr sse sse2 ss ht tm pbe syscall nx pdpe1gb rdtscp lm constant_tsc arch_perfmon pebs bts rep_good nopl xtopology nonstop_tsc aperfmperf eagerfpu pni pclmulqdq dtes64 monitor ds_cpl vmx est tm2 ssse3 fma cx16 xtpr pdcm pcid sse4_1 sse4_2 movbe popcnt tsc_deadline_timer aes xsave avx f16c rdrand lahf_lm abm ida arat epb xsaveopt pln pts dtherm tpr_shadow vnmi flexpriority ept vpid fsgsbase tsc_adjust bmi1 avx2 smep bmi2 erms invpcid
bogomips    : 3591.40
clflush size    : 64
cache_alignment : 64
address sizes   : 39 bits physical, 48 bits virtual
power management:

...

processor   : 3
vendor_id   : GenuineIntel
cpu family  : 6
model       : 69
model name  : Intel(R) Core(TM) i7-4500U CPU @ 1.80GHz
stepping    : 1
microcode   : 0x17
cpu MHz     : 774.000
cache size  : 4096 KB
physical id : 0
siblings    : 4
core id     : 1
cpu cores   : 2
apicid      : 3
initial apicid  : 3
fpu     : yes
fpu_exception   : yes
cpuid level : 13
wp      : yes
flags       : fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush dts acpi mmx fxsr sse sse2 ss ht tm pbe syscall nx pdpe1gb rdtscp lm constant_tsc arch_perfmon pebs bts rep_good nopl xtopology nonstop_tsc aperfmperf eagerfpu pni pclmulqdq dtes64 monitor ds_cpl vmx est tm2 ssse3 fma cx16 xtpr pdcm pcid sse4_1 sse4_2 movbe popcnt tsc_deadline_timer aes xsave avx f16c rdrand lahf_lm abm ida arat epb xsaveopt pln pts dtherm tpr_shadow vnmi flexpriority ept vpid fsgsbase tsc_adjust bmi1 avx2 smep bmi2 erms invpcid
bogomips    : 3591.40
clflush size    : 64
cache_alignment : 64
address sizes   : 39 bits physical, 48 bits virtual
power management:
```

## 4 Comprobar si el núcleo instalado en tu ordenador contiene este módulo del kernel usando la orden `kvm-ok`. 

### Portatil

```bash
$ sudo kvm-ok
INFO: /dev/kvm exists               
KVM acceleration can be used
```



## 5 Darse de alta en servicios de nube usando ofertas gratuitas o cupones que pueda proporcionar el profesor.

Me he dado de alta en [Azure](https://azure.microsoft.com/es-es/) con la subscripción proporcionada por el profesor

