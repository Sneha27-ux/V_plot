# V Plot
The python file V_ploy.py, contains the code to create matrix file for V plot.
To execute is, use the command "cat mapped.bed | python vplot.py mapped.bed matrix_file.txt"

To create the V_plot from the generated matrix file use the command gnuplot -persist -e "set term pngcairo size 1200,800; set output 'matrix_plot.png'; set xlabel 'Relative Distance from Center'; set ylabel 'Fragment Length'; set xrange [-600:600]; set yrange [25:225]; set cblabel 'Count'; set palette defined (0 'blue', 1 'green', 2 'yellow', 3 'red'); set style fill solid 1.0; plot 'matrix_file.txt' using 1:2:3 with points pointtype 7 pointsize 0.3 palette"
