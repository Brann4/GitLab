# GitLab
Informe de GitLab
\documentclass[letterpaper,12pt]{report}
\usepackage[right=2cm,left=3cm,top=2cm,bottom=2cm,footskip=1.4cm]{geometry}%margenes de la pagina
\usepackage{fancyhdr}
\pagestyle{fancy}
\usepackage{tikz}
%\pagestyle{fancyplain}

% \fancyhead[C]{ }
% \fancyhead[R]{\thepage}
% \fancyhead[L]{}
% \fancyfoot[C]{}
\pagestyle{headings} %Se puede seleccionar esta opción o todas las anteriores.
\renewcommand{\headrulewidth}{0pt} % grosor de la línea de la cabecera

\usepackage{ucs}
\usepackage[utf8x]{inputenc}
\usepackage[spanish, es-tabla]{babel}
\usepackage[T1]{fontenc}
\usepackage{graphicx}
\usepackage{multicol} %multicolumnas
\usepackage{subfigure} %incluir multiples imágenes en una figura
% \usepackage[vlined, lined, linesnumbered, algosection]{algorithm2e} %paquete para los algoritmos en pseudocódigo
\usepackage{enumerate} %permite cambiar el item de la enumeracion mas facilmente: \begin{enumerate}[(a)] %for small alpha-characters within brackets.
						%Otra opcion renombrar el item: \renewcommand{\labelenumi}{\Alph{enumi}.}
\RequirePackage{hyperref}
\RequirePackage{url} %citacion de URL
\usepackage{hyperref}
\linespread{1.5} %interlineado

\usepackage{listings}
\lstset{language=C, numbers=left, numberstyle=\small, tabsize=2, captionpos=b, frame=single, breaklines=true, basicstyle=\normalsize, showstringspaces=false}
\renewcommand\lstlistingname{Código}

% Para algoritmos
\usepackage{algorithmic}
\usepackage{algorithm}
\floatname{algorithm}{Algoritmo}
\renewcommand{\listalgorithmname}{Lista de algoritmos}
\renewcommand{\algorithmicrequire}{\textbf{Entrada:}}
\renewcommand{\algorithmicensure}{\textbf{Retorna:}}
\renewcommand{\algorithmicprint}{\textbf{ESCRIBIR}}
\newcommand{\READ}[1]{\STATE \textbf{LEER} (#1)}
\renewcommand{\algorithmicif}{\textbf{si}}
\renewcommand{\algorithmicthen}{\textbf{entonces}}
\renewcommand{\algorithmicelse}{\textbf{sino}}
\renewcommand{\algorithmicfor}{\textbf{para}}
\renewcommand{\algorithmicforall}{\textbf{para todo}}
\renewcommand{\algorithmicdo}{\textbf{hacer}}
\renewcommand{\algorithmicrepeat}{\textbf{repetir}}
\renewcommand{\algorithmicreturn}{\textbf{retornar}}
\renewcommand{\algorithmictrue}{\textbf{verdadero}}
\renewcommand{\algorithmicfalse}{\textbf{falso}}
\renewcommand{\algorithmicend}{\textbf{fin}}
\renewcommand{\algorithmicwhile}{\textbf{mientras}}
\renewcommand{\algorithmiccomment}[1]{//#1}
\renewcommand{\algorithmicendloop}{\algorithmicend\ \algorithmicloop}
\renewcommand{\algorithmicendwhile}{\algorithmicend\ \algorithmicwhile}
\renewcommand{\algorithmicendfor}{\algorithmicend\ \algorithmicfor}
\renewcommand{\algorithmicelsif}{\algorithmicelse,\ \algorithmicif}
\renewcommand{\algorithmicendif}{\algorithmicend\ \algorithmicif}

\begin{document}
\renewcommand{\contentsname}{Tabla de Contenido}
\begin{titlepage}
\begin{center}
\vspace*{0.5in}
UNIVERSIDAD PRIVADA DE TACNA\\
FACULTAD DE INGENIERÍA\\
ESCUELA PROFESIONAL DE INGENIERIA DE SISTEMAS\\
INGENIERÍA DE SISTEMAS

\vspace*{0.5in}
\begin{figure}[htb]
\begin{center}
	\includegraphics[scale=0.5]{GitLab_logo.png}
	% color-836x732.png: 836x732 pixel, 72dpi, 29.50x25.83 cm, bb=0 0 836 732
\end{center}
\end{figure}



\vspace*{0.5in}
\begin{Large}
\textbf{Informe de GitLab} \\
\end{Large}
\vspace*{1in}


\end{center}
\begin{flushright}

\begin{tabular}{lll}
Integrantes & : & Brandon Dennis Mamani Ayala\\
          &   & 2015052715\\ 
Profesor & : & Ing. Patrick Cuadros Quiroga\\
Curso & : & Base de Datos II\\
Fecha & : & \today
\end{tabular}
\end{flushright}
\end{titlepage}

\tableofcontents

\chapter{¿Qu\'e es GitLab?}\label{cap:1}
GitLab nació como un sistema de alojamiento de repositorios Git, es decir, un hosting para proyectos gestionados por el sistema de versiones Git. Sin embargo, alrededor de esta herramienta han surgido muchas otras herramientas muy interesantes para programadores y equipos de desarrollo, que envuelven todo el flujo del desarrollo y el despliegue de aplicaciones, test, etc.

Sin duda, para dar una idea de lo que es GitLab, lo más rápido sería compararlo con uno de sus competidores, GitHub, pues éste último es especialmente conocido en el mundo del desarrollo de software. Todos más o menos estamos familiarizados con lo que ofrece, la gestión de repositorios, las issues, los pull request, GitHub Pages, etc. GitLab sería algo muy similar a lo que encontramos en GitHub, aunque a veces con otros nombres. Otras alternativas de programas o servicios para Git como Bitbucket están muy por detrás en posibilidades.

Aunque GitHub es un mounstruo, en cuanto a número de repositorios y funcionalidad, GitLab ha conseguido llegar aún más lejos, ofreciendo un conjunto más amplio de servicios que harán las delicias no solo de desarrolladores, sino también de devops.

\section{Como usar Gitlab}\label{sec:1}
GitLab es una herramienta basada en Git, que usas de la misma manera que cualquier otra herramienta similar. Generalmente usas Git a través de la línea de comandos, o a través de programas de interfaz gráfica, o del propio editor de código. Toda esa operativa que ya conoces y que hemos explicado en el Manual de Git, no cambia.

Además del hosting remoto para repositorios GitLab ofrece una interfaz web para controlar el repositorio y muchas otras herramientas. Ofrece la posibilidad de examinar el código en cualquiera de sus versiones, realizar acciones relacionadas con el sistema de repositorios como mergear el código de versiones de proyecto o gestionar las "pull request" (que en GitLab se llaman "merge request"), gestionar problemática de tu software diversa, automatizar procesos como el despliegue o la ejecución de pruebas del software, etc. Toda esta operativa la realizas, o configuras, en GitLab por medio de una web.

Por tanto, para usar GitLab simplemente necesitas las mismas herramientas que ya utilizas en tu día a día, el terminal o un programa de interfaz gráfica para gestionar tu repositorio, así como el navegador web para acceder a el ecosistema de herramientas disponible en el sitio de GitLab. Por supuesto, todas estas herramientas las puedes usar desde cualquier ordenador conectado a Internet, independientemente de su sistema operativo.

\section{Funcionalidades de Gitlab}\label{sec:2}
En GitLab podemos gestionar principalmente proyectos, Grupos y Sinppets. Los proyectos son los protagonistas del sistema, básicamente repositorios de software gestionados por GitLab y todo el ecosistema GitLab. Los grupos son básicamente empresas y usuarios. Los snippets por su parte son como pedazos de código que puedes dejar para hacer cualquier cosa.
Como decimos, dentro de los proyectos es donde se aglutinan la mayoría de las funcionalidades que vamos a resumir:

 \begin{enumerate}[a)]
        \item Overview:
           \begin{description}
                 \item 
                     Es un listado de todo el proyecto, los archivos, los README.md. Es parecido a lo que vemos cuando accedemos a un proyecto con GitHub. Te da el resumen del repositorio, archivos, commits, etc.Luego tiene dos subsecciones: En Activity del proyecto te ofrece toda la actividad, de una manera estadística. En Cycle Analytics además te ofrece algo muy novedoso, no disponible en otras herramientas. Básicamente informa el tiempo que se tarda en realizar una funcionalidad, desde que tienes la idea hasta que se incorpora al software, de modo que cualquier persona, incluso sin conocimientos de programación, puede saber el tiempo que ocupó el hacer las tareas. Una información muy valiosa que puede ayudar a futuro a estimar mejor el tiempo de trabajo necesario para nuevas funcionalidades. Obviamente, cuantas más issues tengas en el sistema, más datos tendrás para saber el tiempo que necesitas para las próximas tareas.
            \end{description}
        \item Repository:
            \begin{description}
                \item 
                     Dentro de la sección Repository tenemos varias opciones diversas que afectan al repositorio del proyecto.Tenemos "Files", donde se puede navegar por los directorios y archivos, cuyo código podemos ver, e incluso editar los ficheros. Está disponible una visualización por ramas y dispone de utilidades diversas para poder hacer cosas relacionadas con el repositorio remoto, ahorrando la necesidad de lanzar comandos. Tiene un buscador de archivos muy potente.En "Commits" encontramos un listado de todos los commits realizados contra el repositorio, junto con datos específicos de cada uno de ellos.Las ramas "Branches" sirven para ver las ramas que tenemos en el repositorio.La siguiente sección, "Tags", es importante también, pues es el mecanismo disponible en Git para definir puntos del estado del código, correspondientes a cada release.Además esta sección tiene otras áreas también importantes, que os dejamos para vuestra propia investigación. Especialmente sería destacable la parte de "Locked files", disponible solo en GitLab como servicio, que es algo que no ofrece el propio sistema de control de versiones Git pero que han implementado dentro de GitLab, que permite bloquear un fichero para que solo ciertas personas lo puedan editar.
            \end{description}
        \item Issues:
              \begin{description}
                \item 
                     Este es otra de las grandes utilidades de GitLab, que permite definir cualquier problema que se detecta en el software y darle seguimiento. Seguro que las conocemos porque es una de las partes fundamentales de GitHub y habremos navegado por ellas en decenas de ocasiones.Básicamente nos permite ver las issues generadas en un proyecto, mantener discusiones sobre ellas, y controlar los flujos de trabajo para su resolución, permitiendo definir las personas que deben resolverla, el tiempo estimado y el usado, la fecha límite, el peso de las tareas, etc.En GitLab han publicado otra interesante innovación que es un tablero de issues (Issue Boards), que permite visualizar las tareas, de una manera similar a los boards de Trello. Como gestores somos capaces de definir los tableros y las etiquetas. GitLab, por medio de la gestión de las Issues, es capaz actualizar el estado de las tareas, permitiendo visualizar su evolución por medio de los tableros.Otra cosa muy interesante es el "Service desk", que te ofrece un email que lo puedes proporcionar al cliente. Sin que el cliente se registre en GitLab, ni tenga acceso al proyecto, puede enviar mensajes a ese email, adjuntando texto, imágenes y archivos. GitLab, al recibir el correo, da de alta automáticamente una issue con ese contenido.
            \end{description}
        \item Merge Request:
          \begin{description}
                \item 
                     Son como las Pull Request de GitHub. Te permiten controlar todas las solicitudes de combinación o unión de código de distintas ramas o forks. Es muy importante que los merges se resuelvan mediante la interfaz gráfica, ya que nos ofrece muchas posibilidades interesantes, como automatización de tests, la posibilidad de revisión de los cambios por parte de componentes del equipo, implementar diversas políticas de control sobre el código del proyecto, etc.
            \end{description}
        \item CI/CD:
          \begin{description}
                \item 
                     Es una de las maravillas que dispone GitLab, una herramienta sencilla y muy útil para los procesos de integración continua y despliegue continuo. Existen muchas herramientas que se pueden integrar para automatizar los procesos y llegar a crear flujos de trabajo completamente automatizados. De modo que se lancen los test y si todo va bien se puedan realizar una serie de tareas definida, que pueden llegar a producir el despliegue automático de las aplicaciones.Solo disponer de esta sección es suficiente motivo para pasarse a GitLab. No llega la complejidad de herramientas específicas como Jenkins, pero resuelve de manera muy potente problemas similares.
            \end{description}
\end{enumerate}


    

\chapter{Historia}\label{cap:2}
Inicialmente el producto se publicó como un software completamente libre bajo la licencia MIT. Sin embargo, tras la división del proyecto en julio de 2013 en dos versiones distintas, GitLab CE (Community Edition) y GitLab EE (Enterprise Edition), finalmente en febrero de 2014 GitLab EE se comenzó a desarrollar bajo una licencia propietaria, con características que no están presentes en la versión libre.5​

En enero de 2017, la base de datos del servidor de producción fue eliminada accidentalmente, lo que supuso la pérdida de toda la actividad que se había desarrollado en las 6 horas anteriores.6​

En marzo de 2017, se anunció la compra del servicio de mensajería instantánea Gitter por parte de GitLab, sin que esto supusiera la fusión de ambos servicios, sino que continuarían como proyectos totalmente independientes. Además, la compañía anunció que publicaría el código de la nueva adquisición bajo la licencia MIT antes de junio de 2017.


\end{document}

%AYUDAS:
insertar codigo desde archivo
\lstinputlisting[caption ={DESCRIPCION} , label=cod:pregunta]{SOURCE}

%insertar codigo
\begin{lstlisting}[caption={DESCRIPCION}, label=cod:pregunta]
\end{lstlisting}
