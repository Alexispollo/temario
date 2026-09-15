<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Examen · Medios alternos de solución de conflictos</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Source+Serif+4:opsz,wght@8..60,400;8..60,600;8..60,700&family=IBM+Plex+Sans:wght@400;500;600&display=swap" rel="stylesheet">
<style>
  :root{
    --bg:#F2EFE9;
    --card:#FBF9F5;
    --ink:#262322;
    --ink-soft:#5A5347;
    --border:#DAD3C3;
    --pine:#3B5249;
    --pine-dim:#EDF1EC;
    --rose:#8B5E62;
    --rose-dim:#F5ECEC;
    --success:#3F6B52;
    --success-bg:#E7F0E9;
    --error:#A24E42;
    --error-bg:#F5E9E6;
  }
  *{box-sizing:border-box;}
  body{
    margin:0;
    background:var(--bg);
    color:var(--ink);
    font-family:'IBM Plex Sans', sans-serif;
    line-height:1.55;
    -webkit-font-smoothing:antialiased;
  }
  h1,h2,h3{
    font-family:'Source Serif 4', serif;
    font-weight:600;
    color:var(--pine);
    margin:0;
  }
  .wrap{max-width:720px; margin:0 auto; padding:0 20px 80px;}

  /* header */
  header.hero{
    padding:56px 0 28px;
    border-bottom:1px solid var(--border);
    margin-bottom:8px;
  }
  header.hero h1{font-size:2rem; line-height:1.2; max-width:16ch;}
  header.hero p{color:var(--ink-soft); max-width:56ch; margin-top:14px; font-size:1.02rem;}

  /* sticky progress */
  .status-bar{
    position:sticky; top:0; z-index:10;
    background:rgba(242,239,233,0.92);
    backdrop-filter: blur(6px);
    border-bottom:1px solid var(--border);
    padding:12px 20px;
    display:flex; align-items:center; justify-content:space-between;
    font-size:0.92rem; color:var(--ink-soft);
  }
  .status-bar .grade{
    font-family:'Source Serif 4', serif;
    font-weight:600;
    color:var(--pine);
    font-size:1.05rem;
  }
  .status-bar .grade.low{color:var(--error);}
  .status-inner{max-width:720px; margin:0 auto; display:flex; align-items:center; justify-content:space-between; width:100%;}

  /* sections */
  .block{margin-top:52px;}
  .block > h2{font-size:1.28rem; padding-bottom:10px; border-bottom:2px solid var(--pine);}
  .block > p.intro{color:var(--ink-soft); font-size:0.95rem; margin:10px 0 0;}

  .q{
    background:var(--card);
    border:1px solid var(--border);
    border-radius:4px;
    padding:22px 22px 20px;
    margin-top:22px;
  }
  .q-head{display:flex; gap:12px; align-items:flex-start;}
  .q-num{
    flex:none;
    width:30px; height:30px;
    border-radius:50%;
    background:var(--pine);
    color:#fff;
    font-family:'Source Serif 4', serif;
    font-weight:600;
    font-size:0.95rem;
    display:flex; align-items:center; justify-content:center;
  }
  .q-prompt{font-size:1.02rem; padding-top:3px;}
  .q-type{
    display:inline-block;
    font-size:0.72rem;
    color:var(--rose);
    border:1px solid var(--rose);
    border-radius:20px;
    padding:2px 9px;
    margin-left:8px;
    vertical-align:2px;
    white-space:nowrap;
  }

  .options{margin:16px 0 0 42px; display:flex; flex-direction:column; gap:9px;}
  .opt{
    display:flex; align-items:flex-start; gap:10px;
    padding:9px 12px;
    border:1px solid var(--border);
    border-radius:4px;
    cursor:pointer;
    font-size:0.96rem;
    transition:border-color .15s, background .15s;
  }
  .opt:hover{border-color:var(--rose);}
  .opt input{margin-top:3px; accent-color:var(--pine);}
  .opt.selected{border-color:var(--pine); background:var(--pine-dim);}

  textarea.open-answer{
    width:100%;
    margin:16px 0 0 42px;
    max-width:calc(100% - 42px);
    padding:12px 14px;
    border:1px solid var(--border);
    border-radius:4px;
    font-family:inherit;
    font-size:0.96rem;
    resize:vertical;
    min-height:70px;
    background:#fff;
  }
  textarea.open-answer:focus{outline:2px solid var(--rose); outline-offset:1px;}

  .match-table{margin:16px 0 0 42px; display:flex; flex-direction:column; gap:10px;}
  .match-row{display:flex; align-items:center; gap:14px; flex-wrap:wrap;}
  .match-left{
    flex:1 1 220px;
    font-size:0.95rem;
    padding:8px 12px;
    background:var(--rose-dim);
    border-radius:4px;
    border:1px solid var(--border);
  }
  .match-row select{
    flex:1 1 240px;
    padding:8px 10px;
    border-radius:4px;
    border:1px solid var(--border);
    font-family:inherit;
    font-size:0.94rem;
    background:#fff;
  }
  .match-row select:focus{outline:2px solid var(--rose);}

  /* feedback */
  .feedback{
    margin:16px 0 0 42px;
    padding:12px 14px;
    border-radius:4px;
    font-size:0.92rem;
    display:none;
  }
  .feedback.show{display:block;}
  .feedback.ok{background:var(--success-bg); color:var(--success); border:1px solid var(--success);}
  .feedback.bad{background:var(--error-bg); color:var(--error); border:1px solid var(--error);}
  .feedback .label{font-weight:600; display:block; margin-bottom:4px;}
  .feedback .answer-key{color:var(--ink); font-weight:400; display:block; margin-top:6px;}

  .q.graded.correct{border-color:var(--success);}
  .q.graded.incorrect{border-color:var(--error);}

  /* submit + results */
  .submit-zone{
    margin-top:56px;
    text-align:center;
  }
  button.submit-btn{
    background:var(--pine);
    color:#fff;
    border:none;
    padding:14px 34px;
    font-size:1rem;
    font-family:'IBM Plex Sans', sans-serif;
    font-weight:500;
    border-radius:4px;
    cursor:pointer;
    transition:background .15s;
  }
  button.submit-btn:hover{background:#2c4038;}
  button.submit-btn:disabled{background:#B7B2A6; cursor:default;}
  p.missing-note{color:var(--error); font-size:0.88rem; margin-top:10px; display:none;}
  p.missing-note.show{display:block;}

  .results-panel{
    margin-top:30px;
    padding:26px 24px;
    background:var(--card);
    border:1px solid var(--pine);
    border-radius:4px;
    text-align:center;
  }
  .results-panel .score{
    font-family:'Source Serif 4', serif;
    font-size:2.6rem;
    font-weight:700;
    color:var(--pine);
  }
  .results-panel .score.low{color:var(--error);}
  .results-panel .score-sub{color:var(--ink-soft); font-size:0.95rem; margin-top:4px;}
  .results-panel .msg{margin-top:12px; font-size:0.98rem;}
  button.retry-btn{
    margin-top:18px;
    background:transparent;
    color:var(--pine);
    border:1px solid var(--pine);
    padding:9px 20px;
    border-radius:4px;
    font-family:inherit;
    font-size:0.9rem;
    cursor:pointer;
  }
  button.retry-btn:hover{background:var(--pine-dim);}

  @media (max-width:480px){
    .options, textarea.open-answer, .match-table{margin-left:0;}
    header.hero{padding-top:36px;}
    header.hero h1{font-size:1.6rem;}
  }
</style>
</head>
<body>

<div class="status-bar">
  <div class="status-inner">
    <span id="progressText">0 de 19 respondidas</span>
    <span class="grade" id="gradeDisplay"></span>
  </div>
</div>

<div class="wrap">
  <header class="hero">
    <h1>Medios alternos de solución de conflictos</h1>
    <p>Examen de repaso sobre niveles y tipos de conflicto, respuestas físicas de la emoción, formas de abordar el conflicto, la pirámide de necesidades, posiciones e intereses, tipos de escucha y el marco de la empatía. Responde todo y presiona «Corregir examen» al final.</p>
  </header>

  <form id="examForm">

    <!-- SECTION 1 -->
    <section class="block">
      <h2>Niveles del conflicto</h2>
      <p class="intro">El conflicto puede presentarse en tres niveles distintos según quién esté involucrado.</p>

      <div class="q" data-qid="q1" data-type="mc" data-correct="1">
        <div class="q-head"><span class="q-num">1</span>
          <span class="q-prompt">¿Cuáles son los tres niveles del conflicto?<span class="q-type">Opción múltiple</span></span>
        </div>
        <div class="options">
          <label class="opt"><input type="radio" name="q1" value="0"> Individual, grupal y nacional</label>
          <label class="opt"><input type="radio" name="q1" value="1"> Interno, interpersonal e intergrupal (o social)</label>
          <label class="opt"><input type="radio" name="q1" value="2"> Personal, laboral y colectivo</label>
          <label class="opt"><input type="radio" name="q1" value="3"> Físico, emocional y social</label>
        </div>
        <div class="feedback"></div>
      </div>

      <div class="q" data-qid="q2" data-type="tf" data-correct="false">
        <div class="q-head"><span class="q-num">2</span>
          <span class="q-prompt">Verdadero o falso: cuando dos compañeros de equipo, unidos por un mismo objetivo, no logran ponerse de acuerdo por sus distintas prioridades, se trata de un conflicto interno.<span class="q-type">V/F</span></span>
        </div>
        <div class="options">
          <label class="opt"><input type="radio" name="q2" value="true"> Verdadero</label>
          <label class="opt"><input type="radio" name="q2" value="false"> Falso</label>
        </div>
        <div class="feedback"></div>
      </div>

      <div class="q" data-qid="q3" data-type="match">
        <div class="q-head"><span class="q-num">3</span>
          <span class="q-prompt">Relaciona cada nivel del conflicto con su definición.<span class="q-type">Relación de columnas</span></span>
        </div>
        <div class="match-table">
          <div class="match-row" data-left="Interno" data-correct="a">
            <div class="match-left">Interno</div>
            <select>
              <option value="">Selecciona una definición…</option>
              <option value="b">Ocurre entre dos o más personas ligadas por un objetivo compartido, con intereses que parecen incompatibles</option>
              <option value="c">Se presenta entre grupos o países ligados por un objetivo compartido, con intereses que parecen incompatibles</option>
              <option value="a">Se da dentro del individuo, al tener que decidir entre dos intereses que parecen no poder satisfacerse a la vez</option>
            </select>
          </div>
          <div class="match-row" data-left="Interpersonal" data-correct="b">
            <div class="match-left">Interpersonal</div>
            <select>
              <option value="">Selecciona una definición…</option>
              <option value="c">Se presenta entre grupos o países ligados por un objetivo compartido, con intereses que parecen incompatibles</option>
              <option value="b">Ocurre entre dos o más personas ligadas por un objetivo compartido, con intereses que parecen incompatibles</option>
              <option value="a">Se da dentro del individuo, al tener que decidir entre dos intereses que parecen no poder satisfacerse a la vez</option>
            </select>
          </div>
          <div class="match-row" data-left="Intergrupal o social" data-correct="c">
            <div class="match-left">Intergrupal o social</div>
            <select>
              <option value="">Selecciona una definición…</option>
              <option value="b">Ocurre entre dos o más personas ligadas por un objetivo compartido, con intereses que parecen incompatibles</option>
              <option value="a">Se da dentro del individuo, al tener que decidir entre dos intereses que parecen no poder satisfacerse a la vez</option>
              <option value="c">Se presenta entre grupos o países ligados por un objetivo compartido, con intereses que parecen incompatibles</option>
            </select>
          </div>
        </div>
        <div class="feedback"></div>
      </div>
    </section>

    <!-- SECTION 2 -->
    <section class="block">
      <h2>Tipos de conflicto</h2>
      <p class="intro">Según su origen, los conflictos suelen clasificarse en tres tipos.</p>

      <div class="q" data-qid="q4" data-type="mc" data-correct="2">
        <div class="q-head"><span class="q-num">4</span>
          <span class="q-prompt">¿Cuáles son los tres tipos de conflicto según su origen?<span class="q-type">Opción múltiple</span></span>
        </div>
        <div class="options">
          <label class="opt"><input type="radio" name="q4" value="0"> Falta de comunicación, malentendidos y estrés</label>
          <label class="opt"><input type="radio" name="q4" value="1"> Necesidades económicas, sociales y culturales</label>
          <label class="opt"><input type="radio" name="q4" value="2"> Falsas percepciones, falta de comunicación y necesidades incompatibles</label>
          <label class="opt"><input type="radio" name="q4" value="3"> Diferencias de personalidad, edad y género</label>
        </div>
        <div class="feedback"></div>
      </div>

      <div class="q" data-qid="q5" data-type="open" data-min="1" data-groups='[["falta","comunicacion","comunicarse","informacion","no sabia","desconoc","malentendido no dijo"]]'>
        <div class="q-head"><span class="q-num">5</span>
          <span class="q-prompt">Con tus propias palabras, explica en qué consiste un conflicto causado por «falta de comunicación».<span class="q-type">Pregunta abierta</span></span>
        </div>
        <textarea class="open-answer" placeholder="Escribe tu respuesta…"></textarea>
        <div class="feedback"></div>
      </div>

      <div class="q" data-qid="q6" data-type="match">
        <div class="q-head"><span class="q-num">6</span>
          <span class="q-prompt">Relaciona cada ejemplo con el tipo de conflicto que ilustra.<span class="q-type">Relación de columnas</span></span>
        </div>
        <div class="match-table">
          <div class="match-row" data-left="Karla llora y siente que Miguel prioriza el trabajo sobre ella" data-correct="a">
            <div class="match-left">Karla siente, sin comprobarlo, que Miguel prioriza el trabajo sobre ella</div>
            <select>
              <option value="">Selecciona un tipo…</option>
              <option value="c">Necesidades incompatibles</option>
              <option value="b">Falta de comunicación</option>
              <option value="a">Falsas percepciones / emociones</option>
            </select>
          </div>
          <div class="match-row" data-left="Karina se molesta por la pluma" data-correct="b">
            <div class="match-left">Karina se molesta de que María le pida su pluma, pero nunca se lo ha dicho</div>
            <select>
              <option value="">Selecciona un tipo…</option>
              <option value="b">Falta de comunicación</option>
              <option value="a">Falsas percepciones / emociones</option>
              <option value="c">Necesidades incompatibles</option>
            </select>
          </div>
          <div class="match-row" data-left="Carlos y Fabián, trabajo en equipo entre ciudades" data-correct="c">
            <div class="match-left">Carlos no puede ir a CDMX y Fabián no quiere ir a Toluca para el trabajo en equipo</div>
            <select>
              <option value="">Selecciona un tipo…</option>
              <option value="a">Falsas percepciones / emociones</option>
              <option value="c">Necesidades incompatibles</option>
              <option value="b">Falta de comunicación</option>
            </select>
          </div>
        </div>
        <div class="feedback"></div>
      </div>
    </section>

    <!-- SECTION 3 -->
    <section class="block">
      <h2>Elementos físicos de las emociones</h2>
      <p class="intro">Las emociones se manifiestan también en el cuerpo, no solo en lo que se dice.</p>

      <div class="q" data-qid="q7" data-type="open" data-min="3" data-groups='[["ceja"],["nariz"],["cara","rostro","gesto"],["distancia","alejar","acercar"],["temblor","temblar"],["sonroj","rubor"],["sudor","transpira"],["respiracion","respirar","agitad"],["pupila"],["corazon","cardiaco","palpita","ritmo"]]'>
        <div class="q-head"><span class="q-num">7</span>
          <span class="q-prompt">Menciona al menos tres elementos físicos en los que se manifiestan las emociones.<span class="q-type">Pregunta abierta</span></span>
        </div>
        <textarea class="open-answer" placeholder="Escribe tu respuesta…"></textarea>
        <div class="feedback"></div>
      </div>

      <div class="q" data-qid="q8" data-type="tf" data-correct="false">
        <div class="q-head"><span class="q-num">8</span>
          <span class="q-prompt">Verdadero o falso: el tono y ritmo de la voz es el único elemento físico en el que se manifiesta una emoción durante un conflicto.<span class="q-type">V/F</span></span>
        </div>
        <div class="options">
          <label class="opt"><input type="radio" name="q8" value="true"> Verdadero</label>
          <label class="opt"><input type="radio" name="q8" value="false"> Falso</label>
        </div>
        <div class="feedback"></div>
      </div>
    </section>

    <!-- SECTION 4 -->
    <section class="block">
      <h2>Formas de abordar el conflicto</h2>
      <p class="intro">Cada persona tiende a resolver el conflicto desde un estilo distinto, según priorice el resultado o la relación.</p>

      <div class="q" data-qid="q9" data-type="mc" data-correct="1">
        <div class="q-head"><span class="q-num">9</span>
          <span class="q-prompt">El estilo que busca «ganar a tu manera», aunque el otro pierda, se llama:<span class="q-type">Opción múltiple</span></span>
        </div>
        <div class="options">
          <label class="opt"><input type="radio" name="q9" value="0"> Comprometido / colaborativo</label>
          <label class="opt"><input type="radio" name="q9" value="1"> Competitivo</label>
          <label class="opt"><input type="radio" name="q9" value="2"> Complaciente</label>
        </div>
        <div class="feedback"></div>
      </div>

      <div class="q" data-qid="q10" data-type="mc" data-correct="2">
        <div class="q-head"><span class="q-num">10</span>
          <span class="q-prompt">El estilo que cede ante el otro, priorizando la relación por encima del propio resultado, se llama:<span class="q-type">Opción múltiple</span></span>
        </div>
        <div class="options">
          <label class="opt"><input type="radio" name="q10" value="0"> Comprometido / colaborativo</label>
          <label class="opt"><input type="radio" name="q10" value="1"> Competitivo</label>
          <label class="opt"><input type="radio" name="q10" value="2"> Complaciente</label>
        </div>
        <div class="feedback"></div>
      </div>

      <div class="q" data-qid="q11" data-type="mc" data-correct="1">
        <div class="q-head"><span class="q-num">11</span>
          <span class="q-prompt">El estilo que busca trabajar junto con la otra parte para solucionar el problema y satisfacer a ambos se llama:<span class="q-type">Opción múltiple</span></span>
        </div>
        <div class="options">
          <label class="opt"><input type="radio" name="q11" value="0"> Complaciente</label>
          <label class="opt"><input type="radio" name="q11" value="1"> Comprometido / colaborativo</label>
          <label class="opt"><input type="radio" name="q11" value="2"> Competitivo</label>
        </div>
        <div class="feedback"></div>
      </div>
    </section>

    <!-- SECTION 5 -->
    <section class="block">
      <h2>Pirámide de necesidades (Maslow)</h2>
      <p class="intro">Detrás de un conflicto suele haber necesidades sin resolver, clasificadas por Abraham Maslow en cinco categorías.</p>

      <div class="q" data-qid="q12" data-type="match">
        <div class="q-head"><span class="q-num">12</span>
          <span class="q-prompt">Relaciona cada tipo de necesidad con lo que representa.<span class="q-type">Relación de columnas</span></span>
        </div>
        <div class="match-table">
          <div class="match-row" data-left="Fisiológicas" data-correct="a">
            <div class="match-left">Fisiológicas</div>
            <select>
              <option value="">Selecciona…</option>
              <option value="d">Confianza en uno mismo, prestigio y reconocimiento</option>
              <option value="a">Hambre, sueño, descanso: la supervivencia del individuo</option>
              <option value="c">Amor, afecto y participación con otras personas</option>
              <option value="e">Encontrarle sentido a la propia existencia y desarrollar el potencial</option>
              <option value="b">Protegerse de un peligro real o imaginario (empleo, salud, propiedad)</option>
            </select>
          </div>
          <div class="match-row" data-left="De seguridad" data-correct="b">
            <div class="match-left">De seguridad</div>
            <select>
              <option value="">Selecciona…</option>
              <option value="a">Hambre, sueño, descanso: la supervivencia del individuo</option>
              <option value="c">Amor, afecto y participación con otras personas</option>
              <option value="b">Protegerse de un peligro real o imaginario (empleo, salud, propiedad)</option>
              <option value="d">Confianza en uno mismo, prestigio y reconocimiento</option>
              <option value="e">Encontrarle sentido a la propia existencia y desarrollar el potencial</option>
            </select>
          </div>
          <div class="match-row" data-left="De pertenencia" data-correct="c">
            <div class="match-left">De pertenencia</div>
            <select>
              <option value="">Selecciona…</option>
              <option value="e">Encontrarle sentido a la propia existencia y desarrollar el potencial</option>
              <option value="b">Protegerse de un peligro real o imaginario (empleo, salud, propiedad)</option>
              <option value="d">Confianza en uno mismo, prestigio y reconocimiento</option>
              <option value="c">Amor, afecto y participación con otras personas</option>
              <option value="a">Hambre, sueño, descanso: la supervivencia del individuo</option>
            </select>
          </div>
          <div class="match-row" data-left="De reconocimiento" data-correct="d">
            <div class="match-left">De reconocimiento</div>
            <select>
              <option value="">Selecciona…</option>
              <option value="c">Amor, afecto y participación con otras personas</option>
              <option value="e">Encontrarle sentido a la propia existencia y desarrollar el potencial</option>
              <option value="a">Hambre, sueño, descanso: la supervivencia del individuo</option>
              <option value="b">Protegerse de un peligro real o imaginario (empleo, salud, propiedad)</option>
              <option value="d">Confianza en uno mismo, prestigio y reconocimiento</option>
            </select>
          </div>
          <div class="match-row" data-left="De autorrealización" data-correct="e">
            <div class="match-left">De autorrealización</div>
            <select>
              <option value="">Selecciona…</option>
              <option value="b">Protegerse de un peligro real o imaginario (empleo, salud, propiedad)</option>
              <option value="d">Confianza en uno mismo, prestigio y reconocimiento</option>
              <option value="a">Hambre, sueño, descanso: la supervivencia del individuo</option>
              <option value="e">Encontrarle sentido a la propia existencia y desarrollar el potencial</option>
              <option value="c">Amor, afecto y participación con otras personas</option>
            </select>
          </div>
        </div>
        <div class="feedback"></div>
      </div>

      <div class="q" data-qid="q13" data-type="open" data-min="1" data-groups='[["fisiolog"]]'>
        <div class="q-head"><span class="q-num">13</span>
          <span class="q-prompt">¿Qué tipo de necesidad, según Maslow, se relaciona con el hambre, el sueño y la supervivencia del individuo?<span class="q-type">Pregunta abierta</span></span>
        </div>
        <textarea class="open-answer" placeholder="Escribe tu respuesta…"></textarea>
        <div class="feedback"></div>
      </div>
    </section>

    <!-- SECTION 6 -->
    <section class="block">
      <h2>Posición, interés y necesidad</h2>
      <p class="intro">Lo que las partes dicen que quieren no siempre es lo mismo que realmente necesitan resolver.</p>

      <div class="q" data-qid="q14" data-type="open" data-min="2" data-groups='[["posicion","exigencia","demanda","lo que piden","lo que dicen querer","superficial","inicial"],["interes","necesidad","detras","fondo","subyace","realmente quieren","realmente necesitan"]]'>
        <div class="q-head"><span class="q-num">14</span>
          <span class="q-prompt">Explica con tus palabras la diferencia entre la «posición» de una parte y sus «intereses o necesidades».<span class="q-type">Pregunta abierta</span></span>
        </div>
        <textarea class="open-answer" placeholder="Escribe tu respuesta…"></textarea>
        <div class="feedback"></div>
      </div>

      <div class="q" data-qid="q15" data-type="tf" data-correct="false">
        <div class="q-head"><span class="q-num">15</span>
          <span class="q-prompt">Verdadero o falso: cuando alguien exige la devolución de su dinero en un conflicto, esa exigencia agota por completo lo que necesita para sentirse satisfecho, sin nada más detrás de ella.<span class="q-type">V/F</span></span>
        </div>
        <div class="options">
          <label class="opt"><input type="radio" name="q15" value="true"> Verdadero</label>
          <label class="opt"><input type="radio" name="q15" value="false"> Falso</label>
        </div>
        <div class="feedback"></div>
      </div>
    </section>

    <!-- SECTION 7 -->
    <section class="block">
      <h2>Tipos de escucha</h2>

      <div class="q" data-qid="q16" data-type="mc" data-correct="0">
        <div class="q-head"><span class="q-num">16</span>
          <span class="q-prompt">El tipo de escucha que filtra el mensaje según los propios valores y reacciona juzgando se llama escucha:<span class="q-type">Opción múltiple</span></span>
        </div>
        <div class="options">
          <label class="opt"><input type="radio" name="q16" value="0"> Selectiva</label>
          <label class="opt"><input type="radio" name="q16" value="1"> Pasiva</label>
          <label class="opt"><input type="radio" name="q16" value="2"> Activa</label>
        </div>
        <div class="feedback"></div>
      </div>

      <div class="q" data-qid="q17" data-type="mc" data-correct="2">
        <div class="q-head"><span class="q-num">17</span>
          <span class="q-prompt">El tipo de escucha que implica atención, interés y motivación real hacia lo que dice la otra persona se llama escucha:<span class="q-type">Opción múltiple</span></span>
        </div>
        <div class="options">
          <label class="opt"><input type="radio" name="q17" value="0"> Pasiva</label>
          <label class="opt"><input type="radio" name="q17" value="1"> Selectiva</label>
          <label class="opt"><input type="radio" name="q17" value="2"> Activa</label>
        </div>
        <div class="feedback"></div>
      </div>
    </section>

    <!-- SECTION 8 -->
    <section class="block">
      <h2>Marco teórico de la empatía</h2>
      <p class="intro">La escucha activa se apoya en varias herramientas de comunicación empática.</p>

      <div class="q" data-qid="q18" data-type="match">
        <div class="q-head"><span class="q-num">18</span>
          <span class="q-prompt">Relaciona cada herramienta de la escucha activa con lo que busca lograr.<span class="q-type">Relación de columnas</span></span>
        </div>
        <div class="match-table">
          <div class="match-row" data-left="Hacer preguntas abiertas" data-correct="a">
            <div class="match-left">Hacer preguntas abiertas</div>
            <select>
              <option value="">Selecciona…</option>
              <option value="c">Evitar categorizar la conducta del otro con base en prejuicios</option>
              <option value="a">Ceder el control y dejar que la otra persona guíe con sus propias palabras</option>
              <option value="d">Mantener el intercambio abierto en lugar de imponer la última palabra</option>
              <option value="b">Bajar la intensidad de las emociones fuertes para comprender mejor</option>
              <option value="e">Respetar que cada persona es distinta e individual</option>
            </select>
          </div>
          <div class="match-row" data-left="Avanzar lentamente" data-correct="b">
            <div class="match-left">Avanzar lentamente</div>
            <select>
              <option value="">Selecciona…</option>
              <option value="e">Respetar que cada persona es distinta e individual</option>
              <option value="d">Mantener el intercambio abierto en lugar de imponer la última palabra</option>
              <option value="b">Bajar la intensidad de las emociones fuertes para comprender mejor</option>
              <option value="c">Evitar categorizar la conducta del otro con base en prejuicios</option>
              <option value="a">Ceder el control y dejar que la otra persona guíe con sus propias palabras</option>
            </select>
          </div>
          <div class="match-row" data-left="No juzgar" data-correct="c">
            <div class="match-left">No juzgar</div>
            <select>
              <option value="">Selecciona…</option>
              <option value="a">Ceder el control y dejar que la otra persona guíe con sus propias palabras</option>
              <option value="e">Respetar que cada persona es distinta e individual</option>
              <option value="d">Mantener el intercambio abierto en lugar de imponer la última palabra</option>
              <option value="c">Evitar categorizar la conducta del otro con base en prejuicios</option>
              <option value="b">Bajar la intensidad de las emociones fuertes para comprender mejor</option>
            </select>
          </div>
          <div class="match-row" data-left="No poner fin a la historia" data-correct="d">
            <div class="match-left">No poner fin a la historia</div>
            <select>
              <option value="">Selecciona…</option>
              <option value="b">Bajar la intensidad de las emociones fuertes para comprender mejor</option>
              <option value="c">Evitar categorizar la conducta del otro con base en prejuicios</option>
              <option value="a">Ceder el control y dejar que la otra persona guíe con sus propias palabras</option>
              <option value="e">Respetar que cada persona es distinta e individual</option>
              <option value="d">Mantener el intercambio abierto en lugar de imponer la última palabra</option>
            </select>
          </div>
          <div class="match-row" data-left="Establecer límites" data-correct="e">
            <div class="match-left">Establecer límites</div>
            <select>
              <option value="">Selecciona…</option>
              <option value="c">Evitar categorizar la conducta del otro con base en prejuicios</option>
              <option value="d">Mantener el intercambio abierto en lugar de imponer la última palabra</option>
              <option value="e">Respetar que cada persona es distinta e individual</option>
              <option value="a">Ceder el control y dejar que la otra persona guíe con sus propias palabras</option>
              <option value="b">Bajar la intensidad de las emociones fuertes para comprender mejor</option>
            </select>
          </div>
        </div>
        <div class="feedback"></div>
      </div>

      <div class="q" data-qid="q19" data-type="open" data-min="2" data-groups='[["quien eres"],["que sientes"],["que piensas"],["que te interesa","que mas te interesa","que es lo que mas te interesa"]]'>
        <div class="q-head"><span class="q-num">19</span>
          <span class="q-prompt">Según el marco teórico de la empatía, menciona al menos dos de las preguntas a las que la empatía busca responder.<span class="q-type">Pregunta abierta</span></span>
        </div>
        <textarea class="open-answer" placeholder="Escribe tu respuesta…"></textarea>
        <div class="feedback"></div>
      </div>
    </section>

    <div class="submit-zone">
      <button type="button" class="submit-btn" id="submitBtn">Corregir examen</button>
      <p class="missing-note" id="missingNote">Responde todas las preguntas antes de corregir.</p>
    </div>

    <div class="results-panel" id="resultsPanel" style="display:none;">
      <div class="score" id="scoreValue">10.0</div>
      <div class="score-sub" id="scoreSub">de calificación</div>
      <div class="msg" id="scoreMsg"></div>
      <button type="button" class="retry-btn" id="retryBtn">Intentar de nuevo</button>
    </div>

  </form>
</div>

<script>
(function(){
  const form = document.getElementById('examForm');
  const questions = Array.from(form.querySelectorAll('.q'));
  const progressText = document.getElementById('progressText');
  const gradeDisplay = document.getElementById('gradeDisplay');
  const submitBtn = document.getElementById('submitBtn');
  const missingNote = document.getElementById('missingNote');
  const resultsPanel = document.getElementById('resultsPanel');

  function normalize(s){
    return (s||'').toLowerCase()
      .normalize('NFD').replace(/[\u0300-\u036f]/g,'')
      .replace(/[^a-z0-9\s]/g,' ')
      .replace(/\s+/g,' ')
      .trim();
  }

  function isAnswered(q){
    const type = q.dataset.type;
    if(type === 'mc' || type === 'tf'){
      return !!q.querySelector('input:checked');
    }
    if(type === 'open'){
      const ta = q.querySelector('textarea');
      return normalize(ta.value).length > 0;
    }
    if(type === 'match'){
      const selects = q.querySelectorAll('select');
      return Array.from(selects).every(s => s.value !== '');
    }
    return false;
  }

  function updateProgress(){
    const answered = questions.filter(isAnswered).length;
    progressText.textContent = answered + ' de ' + questions.length + ' respondidas';
  }

  // live "selected" highlight for radio options + progress updates
  questions.forEach(q => {
    q.querySelectorAll('.opt').forEach(opt => {
      const input = opt.querySelector('input');
      if(input){
        input.addEventListener('change', () => {
          opt.parentElement.querySelectorAll('.opt').forEach(o => o.classList.remove('selected'));
          opt.classList.add('selected');
          updateProgress();
        });
      }
    });
    q.querySelectorAll('textarea, select').forEach(el => {
      el.addEventListener('input', updateProgress);
      el.addEventListener('change', updateProgress);
    });
  });

  function gradeQuestion(q){
    const type = q.dataset.type;
    const fb = q.querySelector('.feedback');
    let correct = false;
    let keyText = '';

    if(type === 'mc'){
      const sel = q.querySelector('input:checked');
      const correctIdx = q.dataset.correct;
      correct = sel && sel.value === correctIdx;
      const correctLabel = q.querySelector('.opt input[value="'+correctIdx+'"]').parentElement.textContent.trim();
      keyText = 'Respuesta correcta: ' + correctLabel;
    } else if(type === 'tf'){
      const sel = q.querySelector('input:checked');
      correct = sel && sel.value === q.dataset.correct;
      keyText = 'Respuesta correcta: ' + (q.dataset.correct === 'true' ? 'Verdadero' : 'Falso');
    } else if(type === 'open'){
      const ta = q.querySelector('textarea');
      const norm = normalize(ta.value);
      const groups = JSON.parse(q.dataset.groups);
      const min = parseInt(q.dataset.min, 10);
      let matched = 0;
      groups.forEach(group => {
        if(group.some(kw => norm.includes(normalize(kw)))) matched++;
      });
      correct = matched >= min;
      keyText = 'Se evalúa por conceptos clave, no por texto exacto. Ideas esperadas: ' +
        groups.map(g => g[0]).join(', ') + '.';
    } else if(type === 'match'){
      const rows = q.querySelectorAll('.match-row');
      let total = rows.length, right = 0;
      let wrongLefts = [];
      rows.forEach(row => {
        const select = row.querySelector('select');
        const expected = row.dataset.correct;
        if(select.value === expected){ right++; }
        else { wrongLefts.push(row.dataset.left); }
      });
      correct = (right === total);
      keyText = right + ' de ' + total + ' pares correctos.' +
        (wrongLefts.length ? ' Revisa: ' + wrongLefts.join('; ') + '.' : '');
      // partial credit stored for scoring
      q.dataset.partial = (right / total).toFixed(4);
    }

    q.classList.remove('graded','correct','incorrect');
    q.classList.add('graded', correct ? 'correct' : 'incorrect');
    fb.classList.remove('ok','bad');
    fb.classList.add('show', correct ? 'ok' : 'bad');
    fb.innerHTML = '<span class="label">' + (correct ? 'Correcto.' : 'Incorrecto — aquí está en qué te equivocaste:') + '</span>' +
                    '<span class="answer-key">' + keyText + '</span>';

    return correct;
  }

  submitBtn.addEventListener('click', () => {
    const unanswered = questions.filter(q => !isAnswered(q));
    if(unanswered.length){
      missingNote.classList.add('show');
      unanswered[0].scrollIntoView({behavior:'smooth', block:'center'});
      return;
    }
    missingNote.classList.remove('show');

    let totalPoints = 0;
    let earnedPoints = 0;

    questions.forEach(q => {
      const wasCorrect = gradeQuestion(q);
      totalPoints += 1;
      if(q.dataset.type === 'match'){
        earnedPoints += parseFloat(q.dataset.partial);
      } else {
        earnedPoints += wasCorrect ? 1 : 0;
      }
    });

    // lock the form
    form.querySelectorAll('input, textarea, select, button.submit-btn').forEach(el => el.disabled = true);

    const pct = earnedPoints / totalPoints;
    const grade10 = (pct * 10).toFixed(1);

    gradeDisplay.textContent = 'Calificación: ' + grade10 + '/10';
    gradeDisplay.classList.toggle('low', pct < 0.7);

    document.getElementById('scoreValue').textContent = grade10;
    document.getElementById('scoreValue').classList.toggle('low', pct < 0.7);
    document.getElementById('scoreSub').textContent = 'de calificación (' + Math.round(pct*100) + '% de aciertos)';

    let msg = '';
    if(pct >= 0.9) msg = 'Excelente dominio del tema. Revisa las notas en rojo, si las hay, para pulir detalles.';
    else if(pct >= 0.7) msg = 'Buen resultado. Revisa las preguntas marcadas en rojo para reforzar esos puntos.';
    else msg = 'Conviene repasar el material. Revisa cada pregunta marcada en rojo: ahí se explica en qué te equivocaste.';
    document.getElementById('scoreMsg').textContent = msg;

    resultsPanel.style.display = 'block';
    resultsPanel.scrollIntoView({behavior:'smooth', block:'start'});
  });

  document.getElementById('retryBtn').addEventListener('click', () => {
    location.reload();
  });

  updateProgress();
})();
</script>

</body>
</html>
