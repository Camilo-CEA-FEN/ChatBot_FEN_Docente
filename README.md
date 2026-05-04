<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Informe de Costos y Proyección - Asistente IA FEN</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&display=swap" rel="stylesheet">
    <style>
        body { font-family: 'Inter', sans-serif; }
        .bg-fen-gradient { background: linear-gradient(135deg, #1E3A8A 0%, #3B82F6 100%); }
        .card-shadow { box-shadow: 0 4px 6px -1px rgb(0 0 0 / 0.1), 0 2px 4px -2px rgb(0 0 0 / 0.1); }
        .chart-container { position: relative; height: 300px; width: 100%; }
    </style>
</head>
<body class="bg-slate-50 text-slate-800 antialiased">

    <nav class="bg-fen-gradient text-white p-4 shadow-md">
        <div class="max-w-6xl mx-auto flex justify-between items-center">
            <div class="flex items-center gap-2">
                <span class="font-bold tracking-tighter text-xl">FEN</span>
                <span class="text-blue-200 border-l border-blue-400 pl-2 ml-2 text-sm uppercase tracking-widest">Informe de Inversión</span>
            </div>
            <div class="text-xs font-medium bg-white/10 px-3 py-1 rounded-full">ChatBot FEN Docente</div>
        </div>
    </nav>

    <main class="max-w-6xl mx-auto px-4 py-8">
        
        <!-- RESUMEN EJECUTIVO -->
        <header class="mb-10">
            <h1 class="text-3xl font-extrabold text-slate-900 mb-2">Proyección Financiera: Implementación Voiceflow</h1>
            <p class="text-slate-600">Análisis de escalabilidad basado en planes Pro/Business y frecuencia de uso docente.</p>
        </header>

        <div class="grid grid-cols-1 lg:grid-cols-3 gap-6 mb-8">
            <!-- TARJETAS DE PLANES -->
            <div class="bg-white p-6 rounded-2xl card-shadow border-t-4 border-blue-500">
                <h3 class="text-sm font-bold text-slate-500 uppercase mb-1">Opción A: Plan Pro</h3>
                <div class="text-3xl font-black text-slate-900 mb-4">$60 <span class="text-sm font-normal text-slate-400">USD/mes</span></div>
                <ul class="text-xs space-y-2 text-slate-600">
                    <li class="flex items-center gap-2"> <span class="text-blue-500">●</span> Capacidad: ~80-100 conv.</li>
                    <li class="flex items-center gap-2"> <span class="text-blue-500">●</span> Ideal para pilotaje inicial.</li>
                </ul>
            </div>

            <div class="bg-slate-900 text-white p-6 rounded-2xl shadow-xl border-t-4 border-emerald-500">
                <h3 class="text-sm font-bold text-slate-400 uppercase mb-1">Opción B: Plan Business</h3>
                <div class="text-3xl font-black text-white mb-4">$150 <span class="text-sm font-normal text-slate-500">USD/mes</span></div>
                <ul class="text-xs space-y-2 text-slate-300">
                    <li class="flex items-center gap-2"> <span class="text-emerald-400">●</span> Capacidad: ~120-150 conv.</li>
                    <li class="flex items-center gap-2"> <span class="text-emerald-400">●</span> Mayor seguridad y soporte.</li>
                </ul>
            </div>

            <div class="bg-blue-600 text-white p-6 rounded-2xl shadow-lg">
                <h3 class="text-sm font-bold text-blue-100 uppercase mb-1">Métrica de Consumo</h3>
                <div class="text-3xl font-black text-white mb-4">~$1.00 <span class="text-sm font-normal text-blue-200">USD/conv.</span></div>
                <p class="text-[11px] text-blue-100 italic">Costo estimado basado en tokens de conocimiento y procesamiento IA.</p>
            </div>
        </div>

        <!-- GRÁFICO DE PROYECCIÓN DE DOCENTES -->
        <section class="bg-white rounded-3xl p-8 card-shadow border border-slate-200 mb-8">
            <div class="flex flex-col md:flex-row justify-between items-start md:items-center mb-8 gap-4">
                <div>
                    <h2 class="text-2xl font-bold text-slate-800">Escalabilidad de Servicio</h2>
                    <p class="text-sm text-slate-500">¿A cuántos docentes podemos servir según su intensidad de uso?</p>
                </div>
                <div class="flex gap-4">
                    <div class="flex items-center gap-2">
                        <span class="w-3 h-3 bg-blue-500 rounded-full"></span>
                        <span class="text-xs font-medium">Plan Pro ($60)</span>
                    </div>
                    <div class="flex items-center gap-2">
                        <span class="w-3 h-3 bg-slate-800 rounded-full"></span>
                        <span class="text-xs font-medium">Plan Business ($150)</span>
                    </div>
                </div>
            </div>

            <div class="chart-container">
                <canvas id="projectionChart"></canvas>
            </div>
            
            <div class="mt-8 grid grid-cols-1 md:grid-cols-3 gap-4 text-center">
                <div class="p-4 bg-slate-50 rounded-xl">
                    <p class="text-[10px] text-slate-400 uppercase font-bold">Uso Ligero</p>
                    <p class="text-lg font-bold text-slate-800">3 veces/mes</p>
                    <p class="text-xs text-blue-600">Hasta 30-45 docentes</p>
                </div>
                <div class="p-4 bg-slate-50 rounded-xl border-x border-slate-200">
                    <p class="text-[10px] text-slate-400 uppercase font-bold">Uso Medio</p>
                    <p class="text-lg font-bold text-slate-800">5 veces/mes</p>
                    <p class="text-xs text-blue-600">Hasta 18-28 docentes</p>
                </div>
                <div class="p-4 bg-slate-50 rounded-xl">
                    <p class="text-[10px] text-slate-400 uppercase font-bold">Uso Intensivo</p>
                    <p class="text-lg font-bold text-slate-800">7 veces/mes</p>
                    <p class="text-xs text-blue-600">Hasta 13-20 docentes</p>
                </div>
            </div>
        </section>

        <!-- CONCLUSIÓN Y RECOMENDACIÓN -->
        <section class="grid grid-cols-1 md:grid-cols-2 gap-6">
            <div class="bg-emerald-50 border border-emerald-100 p-6 rounded-2xl">
                <h3 class="text-emerald-900 font-bold mb-2 flex items-center gap-2">
                    <span>&#x1F4A1;</span> Recomendación Estratégica
                </h3>
                <p class="text-sm text-emerald-800 leading-relaxed">
                    Se sugiere iniciar con el <strong>Plan Pro ($60)</strong> para un grupo piloto de 15 a 20 docentes con uso moderado. Esto permite validar la tasa de conversión real y ajustar la base de conocimientos antes de escalar a un plan Business.
                </p>
            </div>
            <div class="bg-amber-50 border border-amber-100 p-6 rounded-2xl">
                <h3 class="text-amber-900 font-bold mb-2 flex items-center gap-2">
                    <span>&#x26A0;</span> Variable de Control
                </h3>
                <p class="text-sm text-amber-800 leading-relaxed">
                    El costo de $1 USD por conversación es una estimación conservadora. Si las consultas son breves, la capacidad del Plan Pro podría aumentar hasta un 20%, permitiendo mayor cobertura.
                </p>
            </div>
        </section>

    </main>

    <script>
        const initChart = () => {
            const ctx = document.getElementById('projectionChart').getContext('2d');
            
            // Datos calculados:
            // Plan Pro (~90 conv): 3 veces -> 30 docentes | 5 veces -> 18 docentes | 7 veces -> 13 docentes
            // Plan Bus (~140 conv): 3 veces -> 46 docentes | 5 veces -> 28 docentes | 7 veces -> 20 docentes

            new Chart(ctx, {
                type: 'bar',
                data: {
                    labels: ['3 Usos/Mes (Ligero)', '5 Usos/Mes (Medio)', '7 Usos/Mes (Intensivo)'],
                    datasets: [
                        {
                            label: 'Docentes cubiertos (Plan Pro)',
                            data: [30, 18, 13],
                            backgroundColor: '#3B82F6',
                            borderRadius: 8,
                            barThickness: 40
                        },
                        {
                            label: 'Docentes cubiertos (Plan Business)',
                            data: [46, 28, 20],
                            backgroundColor: '#1E293B',
                            borderRadius: 8,
                            barThickness: 40
                        }
                    ]
                },
                options: {
                    responsive: true,
                    maintainAspectRatio: false,
                    plugins: {
                        legend: { display: false },
                        tooltip: {
                            callbacks: {
                                label: (context) => ` Capacidad: ${context.raw} docentes`
                            }
                        }
                    },
                    scales: {
                        y: {
                            beginAtZero: true,
                            title: { display: true, text: 'Número de Docentes', font: { size: 10 } },
                            grid: { color: '#f1f5f9' }
                        },
                        x: {
                            grid: { display: false }
                        }
                    }
                }
            });
        };

        window.onload = initChart;
    </script>
</body>
</html>
