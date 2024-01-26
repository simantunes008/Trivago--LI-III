CC=gcc
CFLAGS=-Wall -Iinclude `pkg-config --cflags glib-2.0`
LDFLAGS=`pkg-config --libs glib-2.0` -lm

OBJ_DIR=obj
$(shell mkdir -p $(OBJ_DIR))

EXECUTABLES=programa-principal programa-testes

all: $(EXECUTABLES)

programa-principal: $(OBJ_DIR)/main.o $(OBJ_DIR)/parser.o $(OBJ_DIR)/date.o $(OBJ_DIR)/users.o $(OBJ_DIR)/flights.o $(OBJ_DIR)/reservations.o $(OBJ_DIR)/passengers.o $(OBJ_DIR)/users_catalog.o $(OBJ_DIR)/flights_catalog.o $(OBJ_DIR)/reservations_catalog.o $(OBJ_DIR)/passengers_catalog.o $(OBJ_DIR)/statistics.o $(OBJ_DIR)/queries.o $(OBJ_DIR)/executer.o $(OBJ_DIR)/output.o $(OBJ_DIR)/menus.o $(OBJ_DIR)/pages.o
	$(CC) $(CFLAGS) $^ $(LDFLAGS) -o $@

programa-testes: $(OBJ_DIR)/main_tests.o $(OBJ_DIR)/parser.o $(OBJ_DIR)/date.o $(OBJ_DIR)/users.o $(OBJ_DIR)/flights.o $(OBJ_DIR)/reservations.o $(OBJ_DIR)/passengers.o $(OBJ_DIR)/users_catalog.o $(OBJ_DIR)/flights_catalog.o $(OBJ_DIR)/reservations_catalog.o $(OBJ_DIR)/passengers_catalog.o $(OBJ_DIR)/statistics.o $(OBJ_DIR)/executer_tests.o $(OBJ_DIR)/queries_tests.o $(OBJ_DIR)/output.o
	$(CC) $(CFLAGS) $^ $(LDFLAGS) -o $@

$(OBJ_DIR)/main.o: src/main.c
	$(CC) $(CFLAGS) -c $< -o $@
	
$(OBJ_DIR)/main_tests.o: src/main_tests.c
	$(CC) $(CFLAGS) -c $< -o $@

$(OBJ_DIR)/parser.o: src/parser.c
	$(CC) $(CFLAGS) -c $< -o $@

$(OBJ_DIR)/date.o: src/date.c
	$(CC) $(CFLAGS) -c $< -o $@

$(OBJ_DIR)/users.o: src/users.c
	$(CC) $(CFLAGS) -c $< -o $@

$(OBJ_DIR)/flights.o: src/flights.c
	$(CC) $(CFLAGS) -c $< -o $@

$(OBJ_DIR)/reservations.o: src/reservations.c
	$(CC) $(CFLAGS) -c $< -o $@

$(OBJ_DIR)/passengers.o: src/passengers.c
	$(CC) $(CFLAGS) -c $< -o $@

$(OBJ_DIR)/users_catalog.o: src/users_catalog.c
	$(CC) $(CFLAGS) -c $< -o $@

$(OBJ_DIR)/flights_catalog.o: src/flights_catalog.c
	$(CC) $(CFLAGS) -c $< -o $@

$(OBJ_DIR)/reservations_catalog.o: src/reservations_catalog.c
	$(CC) $(CFLAGS) -c $< -o $@

$(OBJ_DIR)/passengers_catalog.o: src/passengers_catalog.c
	$(CC) $(CFLAGS) -c $< -o $@

$(OBJ_DIR)/statistics.o: src/statistics.c
	$(CC) $(CFLAGS) -c $< -o $@

$(OBJ_DIR)/executer.o: src/executer.c
	$(CC) $(CFLAGS) -c $< -o $@

$(OBJ_DIR)/executer_tests.o: src/executer_tests.c
	$(CC) $(CFLAGS) -c $< -o $@

$(OBJ_DIR)/queries.o: src/queries.c
	$(CC) $(CFLAGS) -c $< -o $@

$(OBJ_DIR)/queries_tests.o: src/queries_tests.c
	$(CC) $(CFLAGS) -c $< -o $@

$(OBJ_DIR)/output.o: src/output.c
	$(CC) $(CFLAGS) -c $< -o $@

$(OBJ_DIR)/menus.o: src/menus.c
	$(CC) $(CFLAGS) -c $< -o $@

$(OBJ_DIR)/pages.o: src/pages.c
	$(CC) $(CFLAGS) -c $< -o $@

clean:
	rm -f programa-principal programa-testes $(OBJ_DIR)/*.o
	rm -rf $(OBJ_DIR)
	rm -f Resultados/*.csv Resultados/*.txt
