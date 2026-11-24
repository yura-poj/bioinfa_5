Домашнее задание 5
Строка 29
Пожидаев Юрий Сергеевич

Предсказатели: RoseTTAFold2 и AlphaFold2 через ColabFold.
Выравнивание: jFATCAT-rigid, официальный веб-сервис RCSB.
Визуализация: PyMOL 3.2.0a.

ОТЧЁТ И ПОСЛЕДОВАТЕЛЬНОСТЬ
report_row29.pdf – отчёт с методами, результатами, изображениями и выводами.
sequence.fasta – исходная последовательность из 100 аминокислот.

ВЫПОЛНЕННЫЕ НОУТБУКИ
notebooks/RoseTTAFold2.executed.ipynb и notebooks/AlphaFold2.executed.ipynb – исходные ячейки и сохранённые выводы, выделенные из общей выполненной Colab-сессии по предсказателям.

ПРЕДСКАЗАННЫЕ СТРУКТУРЫ
predictions/rosettafold2.pdb – оригинал RoseTTAFold2, цепь A.
predictions/alphafold2_rank1.pdb – оригинал лучшей модели AlphaFold2, model_4_seed_000, цепь A.

ВЫРАВНИВАНИЕ
alignment/request.json – запрос сервиса.
alignment/response.json – полный успешный ответ RCSB, включая оценки, диапазоны остатков и матрицы преобразования.
alignment/superposition.pdb – структуры после преобразования RCSB: цепь A соответствует RoseTTAFold2, цепь B – AlphaFold2. Дополнительное выравнивание в PyMOL не проводилось.
alignment/rosettafold2.bcif и alignment/alphafold2_rank1.bcif – структуры, возвращённые RCSB после конвертации загруженных PDB.
Временная ссылка RCSB истекла. Успешный результат сохранён в response.json, снимок страницы – в visualization/rcsb_screenshot.jpg.

ВИЗУАЛИЗАЦИЯ
visualization/row29_alignment.pse – сессия PyMOL с обеими структурами и двумя ракурсами: 01_overview и 02_rotated.
RoseTTAFold2, цепь A, окрашен в оранжевый цвет; AlphaFold2, цепь B, в зелёный.
visualization/alignment_overview.png и visualization/alignment_rotated.png – изображения из этой сессии.
visualization/plddt_comparison.png – график локальной уверенности моделей.
visualization/rcsb_screenshot.jpg – неизменённый снимок страницы RCSB с метриками и раскрашенным выравниванием.

ЖУРНАЛЫ
logs/rosettafold2_console.txt и logs/alphafold2_console.txt – исходные выводы ячеек установки и предсказания.
logs/alignment_console.txt – вывод обращения к сервису выравнивания.

ВЫВОД
Модели совпадают частично: RMSD 5,42 Å, TM-score 0,27, 60 сопоставленных пар из 100 остатков. Независимый пересчёт даёт RMSD 5,4203 Å. Общий спиральный участок согласуется лучше, чем протяжённые неспиральные участки. Уверенность предсказаний на многих позициях ограничена; экспериментальной структуры для выбора правильной модели нет.
