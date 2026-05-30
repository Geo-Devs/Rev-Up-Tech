# Rev-Up-Tech
Rev Up Tech



<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mundo Motos | Rev-Up Tech</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600&family=Orbitron:wght@500;700;900&display=swap" rel="stylesheet">
    <link href="https://fonts.googleapis.com/icon?family=Material+Icons+Round" rel="stylesheet">

    <style>
        :root {
            /* Mapeo Cromático Invertido Premium de Base Roja */
            --bg-deep: #4A0505;           /* Fondo Carmesí Profundo satinado (no cansa la vista) */
            --bg-graphite: #0B0B0B;       /* Superficies internas en Negro Profundo Mate */
            --primary-neon: #FF1E1E;      /* Rojo neón de acento de marca */
            --text-pure: #FFFFFF;         /* Contraste perfecto para lecturas principales */
            --text-metallic: #D2D2D6;     /* Subtextos claros optimizados para fondo oscuro */
            --border-steel: rgba(255, 255, 255, 0.12); /* Bordes acero semitransparentes */
            --font-tech: 'Orbitron', sans-serif;
            --font-body: 'Inter', sans-serif;
        }

        body {
            /* Degradado de alta gama para dar textura orgánica al fondo rojo */
            background: linear-gradient(180deg, #3B0303 0%, #5E0707 50%, #2B0202 100%);
            background-attachment: fixed;
            color: var(--text-pure);
            font-family: var(--font-body);
        }

        h1, h2, h3, .navbar-brand {
            font-family: var(--font-tech);
            letter-spacing: 1px;
        }

        /* Navbar Adaptado al Entorno Carmesí */
        .navbar {
            background-color: rgba(11, 11, 11, 0.92);
            border-bottom: 1px solid var(--border-steel);
            padding: 15px 0;
            backdrop-filter: blur(12px);
        }
        .brand-highlight {
            color: var(--primary-neon);
        }
        .nav-link {
            color: var(--text-pure) !important;
            font-family: var(--font-tech);
            font-size: 0.9rem;
            margin-left: 20px;
            transition: color 0.2s ease;
        }
        .nav-link:hover, .nav-link.active {
            color: var(--primary-neon) !important;
        }

        /* Banner Principal Moto con Fusión Oscura */
        .page-banner {
            background: linear-gradient(135deg, rgba(11, 11, 11, 0.85) 0%, rgba(74, 5, 5, 0.4) 100%);
            border-bottom: 1px solid var(--border-steel);
            padding: 80px 0 60px 0;
            position: relative;
        }
        .page-banner::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            height: 3px;
            background: linear-gradient(90deg, var(--text-pure), transparent);
        }

        /* Grid de Servicios Motos (Contraste Flotante Negro sobre Rojo) */
        .service-card {
            background-color: var(--bg-graphite);
            border: 1px solid var(--border-steel);
            border-radius: 12px;
            padding: 35px;
            height: 100%;
            transition: all 0.3s cubic-bezier(0.25, 0.8, 0.25, 1);
        }
        .service-card:hover {
            border-color: var(--text-pure);
            transform: translateY(-5px);
        }
        .service-icon-box {
            width: 60px;
            height: 60px;
            background-color: var(--primary-neon);
            border: 1px solid var(--primary-neon);
            border-radius: 8px;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-bottom: 25px;
            transition: all 0.3s ease;
        }
        .service-card:hover .service-icon-box {
            background-color: transparent;
            border-color: var(--text-pure);
        }
        .service-card:hover .service-icon-box span {
            color: var(--text-pure) !important;
        }
        .service-icon-box span {
            font-size: 2rem;
            color: var(--text-pure);
            transition: color 0.3s ease;
        }

        /* Formulario Limpio Premium Invertido */
        .form-custom {
            background-color: var(--bg-graphite);
            border: 1px solid var(--border-steel);
            border-radius: 14px;
            padding: 40px;
        }
        .form-custom .form-control, .form-custom .form-select {
            background-color: #161618;
            border: 1px solid var(--border-steel);
            color: var(--text-pure);
            padding: 12px 18px;
            transition: all 0.25s ease;
        }
        .form-custom .form-control:focus, .form-custom .form-select:focus {
            border-color: var(--text-pure);
            background-color: #1c1c1e;
            color: var(--text-pure);
            box-shadow: none;
        }
        .form-custom label {
            font-size: 0.85rem;
            text-uppercase: uppercase;
            letter-spacing: 1.5px;
            color: var(--text-metallic);
            margin-bottom: 8px;
            font-weight: 600;
        }

        /* Botón Blanco Elegante de Alto Impacto para Fondo Rojo */
        .btn-neon {
            background-color: var(--text-pure);
            color: #0B0B0B;
            font-family: var(--font-tech);
            font-weight: 800;
            padding: 14px 30px;
            border: 2px solid var(--text-pure);
            border-radius: 6px;
            text-transform: uppercase;
            transition: all 0.25s ease;
            box-shadow: none !important;
        }
        .btn-neon:hover {
            background-color: transparent;
            color: var(--text-pure);
            border-color: var(--text-pure);
        }

        /* Modal Personalizado */
        .modal-content-custom {
            background-color: var(--bg-graphite);
            border: 1px solid var(--border-steel);
            color: var(--text-pure);
            border-radius: 12px;
        }

        /* Footer Sólido */
        footer {
            background-color: #0B0B0B;
            border-top: 1px solid var(--border-steel);
            padding: 45px 0;
        }
        footer a {
            color: var(--text-metallic);
            text-decoration: none;
            transition: color 0.2s ease;
        }
        footer a:hover {
            color: var(--primary-neon);
        }
    </style>
</head>
<body>

    <nav class="navbar navbar-expand-lg navbar-dark sticky-top">
        <div class="container">
            <a class="navbar-brand fw-bold fs-3" href="index.html">
                REV<span class="brand-highlight">-</span>UP TECH
            </a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse justify-content-end" id="navbarNav">
                <ul class="navbar-nav">
                    <li class="nav-item"><a class="nav-link" href="index.html">Inicio</a></li>
                    <li class="nav-item"><a class="nav-link" href="autos.html">Mundo Autos</a></li>
                    <li class="nav-item"><a class="nav-link active" href="motos.html">Mundo Motos</a></li>
                </ul>
            </div>
        </div>
    </nav>

    <header class="page-banner">
        <div class="container">
            <div class="row align-items-center">
                <div class="col-md-8">
                    <span class="text-uppercase text-white fw-bold small tracking-wider" style="letter-spacing: 2px; background: rgba(255,30,30,0.3); padding: 4px 10px; border-radius: 4px;">División 2 Ruedas</span>
                    <h1 class="fw-bold mt-3 mb-3 fs-1">Soluciones de Software para Motocicletas</h1>
                    <p class="text-metallic m-0 fs-5">Plataforma dinámica de alta velocidad optimizada para la gestión ágil de motos y repuestos.</p>
                </div>
            </div>
        </div>
    </header>

    <main class="container py-5">
        <div class="row g-4 mb-5">
            
            <div class="col-md-6">
                <div class="service-card">
                    <div class="service-icon-box">
                        <span class="material-icons-round">bolt</span>
                    </div>
                    <h3 class="h4 text-uppercase fw-bold mb-3">Agendamiento Express</h3>
                    <p class="text-metallic m-0 lh-lg">
                        Sistema ultrarrápido y dinámico de asignación de turnos mecánicos. Optimizado para servicios rápidos de motocicletas (cambios de aceite, pastillas de freno, llantas) incluyendo alertas automáticas por SMS/WhatsApp en tiempo real.
                    </p>
                </div>
            </div>

            <div class="col-md-6">
                <div class="service-card">
                    <div class="service-icon-box">
                        <span class="material-icons-round">motorcycle</span>
                    </div>
                    <h3 class="h4 text-uppercase fw-bold mb-3">Catálogo de Repuestos Moto</h3>
                    <p class="text-metallic m-0 lh-lg">
                        Módulo de e-commerce y compras en línea optimizado visualmente para la venta de accesorios, cascos y repuestos rápidos por marca, cilindraje y compatibilidad de motor específica.
                    </p>
                </div>
            </div>

            <div class="col-md-6">
                <div class="service-card">
                    <div class="service-icon-box">
                        <span class="material-icons-round">published_with_changes</span>
                    </div>
                    <h3 class="h4 text-uppercase fw-bold mb-3">Stock e Inventarios Automatizados</h3>
                    <p class="text-metallic m-0 lh-lg">
                        Control exhaustivo de existencias críticas enfocado en lubricentros y talleres de motos. Permite rastrear líquidos, kits de arrastre y componentes de alta demanda con actualización automatizada por ventas de mostrador.
                    </p>
                </div>
            </div>

            <div class="col-md-6">
                <div class="service-card">
                    <div class="service-icon-box">
                        <span class="material-icons-round">speed</span>
                    </div>
                    <h3 class="h4 text-uppercase fw-bold mb-3">Historial por Intervalos</h3>
                    <p class="text-metallic m-0 lh-lg">
                        Registro clínico estructurado y segmentado rigurosamente por intervalos específicos de kilometraje recomendados para vehículos de dos ruedas (ej. alertas automáticas preventivas cada 3,000 km o 5,000 km).
                    </p>
                </div>
            </div>
        </div>

        <hr class="my-5" style="border-color: var(--border-steel);">

        <div class="row justify-content-center py-4">
            <div class="col-lg-8">
                <div class="text-center mb-4">
                    <h2 class="text-uppercase fw-bold">Simulador de Agendamiento Rev-Up</h2>
                    <p class="text-metallic">Comprueba el funcionamiento de la validación interactiva de nuestra plataforma.</p>
                </div>

                <form id="appointmentForm" class="form-custom" novalidate>
                    <div class="row g-3">
                        <div class="col-md-6">
                            <label for="clientName">Nombre Completo</label>
                            <input type="text" id="clientName" class="form-control" required placeholder="Ej. Juan Pérez">
                        </div>
                        <div class="col-md-6">
                            <label for="motoModel">Modelo / Cilindraje de Moto</label>
                            <input type="text" id="motoModel" class="form-control" required placeholder="Ej. Yamaha R6 600cc">
                        </div>
                        <div class="col-md-6">
                            <label for="serviceType">Tipo de Servicio Express</label>
                            <select id="serviceType" class="form-select" required>
                                <option value="" selected disabled>Seleccionar Mantenimiento...</option>
                                <option value="Cambio de Aceite & Filtro">Cambio de Aceite & Filtro</option>
                                <option value="Ajuste de Kit de Arrastre">Ajuste de Kit de Arrastre</option>
                                <option value="Revisión de Frenos Express">Revisión de Frenos Express</option>
                                <option value="Diagnóstico Eléctrico Completo">Diagnóstico Eléctrico Completo</option>
                            </select>
                        </div>
                        <div class="col-md-6">
                            <label for="appointmentDate">Fecha Solicitada</label>
                            <input type="date" id="appointmentDate" class="form-control" required>
                        </div>
                        <div class="col-12 mt-4">
                            <button type="submit" class="btn btn-neon w-100 py-3 text-uppercase fw-bold" style="letter-spacing: 1px;">
                                Procesar y Agendar Cita
                            </button>
                        </div>
                    </div>
                </form>
            </div>
        </div>
    </main>

    <div class="modal fade" id="successModal" tabindex="-1" aria-hidden="true">
        <div class="modal-dialog modal-dialog-centered">
            <div class="modal-content modal-content-custom">
                <div class="modal-header border-0">
                    <h5 class="modal-title font-tech fw-bold text-uppercase text-danger">Registro Completado</h5>
                    <button type="button" class="btn-close btn-close-white" data-bs-dismiss="modal" aria-label="Close"></button>
                </div>
                <div class="modal-body text-center py-4">
                    <span class="material-icons-round text-success mb-3" style="font-size: 4rem;">check_circle</span>
                    <h4 class="fw-bold mb-2" id="modalTitleClient">¡Cita Agendada Exitosamente!</h4>
                    <p class="text-metallic m-0 px-3" id="modalBodyDetails">
                        El sistema de Rev-Up Tech ha procesado su solicitud correctamente. Su bahía express ha sido reservada.
                    </p>
                </div>
                <div class="modal-footer border-0 justify-content-center">
                    <button type="button" class="btn btn-neon px-4" data-bs-dismiss="modal" style="background-color: var(--primary-neon); color: white; border: none;">Confirmar & Salir</button>
                </div>
            </div>
        </div>
    </div>

    <footer class="text-center text-md-start">
        <div class="container">
            <div class="row g-4 align-items-center">
                <div class="col-md-6">
                    <h5 class="fw-bold text-white font-tech mb-2">REV-UP TECH</h5>
                    <p class="text-metallic m-0">Optimización digital e ingeniería de software automotriz.</p>
                </div>
                <div class="col-md-6 text-md-end">
                    <div class="mb-3">
                        <a href="index.html" class="me-3">Inicio</a>
                        <a href="autos.html" class="me-3">Autos</a>
                        <a href="#">Soporte</a>
                    </div>
                    <p class="text-metallic small m-0">&copy; 2026 Rev-Up Tech. Todos los derechos reservados.</p>
                </div>
            </div>
        </div>
    </footer>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js"></script>

    <script>
        document.getElementById('appointmentForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            const form = e.target;
            const nameInput = document.getElementById('clientName');
            const serviceSelect = document.getElementById('serviceType');
            const dateInput = document.getElementById('appointmentDate');

            if (!form.checkValidity()) {
                form.classList.add('was-validated');
                alert("Por favor, rellene todos los campos requeridos con datos válidos.");
                return;
            }

            const clientName = nameInput.value;
            const serviceSelected = serviceSelect.value;
            const dateFormatted = dateInput.value;

            document.getElementById('modalTitleClient').innerText = `¡Cita Exitosa, ${clientName}!`;
            document.getElementById('modalBodyDetails').innerHTML = `Su servicio de <strong>${serviceSelected}</strong> ha sido agendado correctamente en la plataforma para la fecha <strong>${dateFormatted}</strong>.<br><br><span class="text-danger font-tech small" style="color: #FF1E1E !important;">Bahía Express Asignada y Notificada.</span>`;

            const trackingModal = new bootstrap.Modal(document.getElementById('successModal'));
            trackingModal.show();

            form.reset();
            form.classList.remove('was-validated');
        });
    </script>
</body>
</html>