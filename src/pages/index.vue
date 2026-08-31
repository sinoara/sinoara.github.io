<template>
    <div>
        <div class="text-4xl text-center">Experiência Profissional</div>
        <v-timeline side="end" align="start">
            <v-timeline-item v-for="job in jobs">
                <template v-slot:opposite>{{ job['period'] }}</template>
                <v-card :title="job['position']" :subtitle="job['company']">
                    <v-card-text>
                        <ul>
                            <li v-for="item in job['description']">
                                {{ item }}
                            </li>
                        </ul>
                    </v-card-text>
                </v-card>
            </v-timeline-item>
        </v-timeline>
    </div>
</template>

<script lang="ts" setup>
let jobs: any[] = [
    {
        "position": "Técnico em Automação",
        "company": "RB Automação",
        "period": "10/2025 - atualmente",
        "description": [
            "Programação de CLP e IHM",
            "Montagem de painéis elétricos",
            "Desenvolvimento de produtos de automação residencial em Python(Django) e Dart(Flutter)",
            "Solução de problemas em sistemas elétricos",
            "Auxílio em instalações elétricas",
            "Escrita de documentação técnica",
        ],
    },
    {
        "position": "Professor Particular",
        "company": null,
        "period": "03/2024 - 10/2025",
        "description": [
            "Matemática",
            "Física",
            "Inglês",
        ],
    },
    {
        "position": "Arquiteto de Sistemas de Controle",
        "company": "Elemental Future GmbH - Munique, Alemanha",
        "period": "11/2020 - 03/2022",
        "description": [
            "Integração de software para simulação de dinâmica de voo e piloto automático",
            "Projeto e implementação de sistema de controle para aeronave autônoma",
            "Projeto e implementação de sistema fly-by-wire baseado em Arduino",
            "Projeto e implementação de sistema de comunicação baseado em wi-fi para aeróstato cativo",
        ],
    },
    {
        "position": "Engenheiro Aeronáutico",
        "company": "Airship do Brasil",
        "period": "01/2014 - 14/2019",
        "description": [
            "Desenvolvimento de modelos de dinâmica de voo, estrutural e aerodinâmico para projeto de aeronaves em MATLAB e Simulink",
            "Reprojeto de sistemas e substanciação para certificação",
            "Escrita de procedimentos de produção",
            "Revisão de desenhos de produção",
            "Integração de aeronave experimental",
            "Suporte técnico em casos de desvios de produção",
        ],
    },
]
</script>
