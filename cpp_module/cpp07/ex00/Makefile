NAME		=	ex00

SRC_FILES	=	main.cpp

SRC_DIR		=	src/

SCRS		=	$(addprefix $(SRC_DIR), $(SRC_FILES))

OBJ_DIR		=	obj/

OBJS		=	$(addprefix $(OBJ_DIR), $(patsubst %.cpp,%.o,$(SRC_FILES)))

CC			=	c++

FLAGS		=	-Wall -Wextra -Werror -std=c++98

RESET		=	\033[0m
BLACK		=	\033[30m
RED			=	\033[31m
GREEN		=	\033[32m
YELLOW		=	\033[33m
BLUE		=	\033[34m
PURPLE		=	\033[35m
CYAN		=	\033[36m
WHITE		=	\033[37m
UP			=	\033[A
CUT			=	\033[K

all: $(NAME)


$(NAME): $(OBJS)
	@echo "$(CYAN)Compiling...        [$(NAME)]$(RESET)"
	@$(CC) $(FLAGS) $(OBJS) -o $(NAME)
	@echo "$(GREEN)Make success!       [$(NAME)]$(RESET)"

	@printf "\n"
	@printf "$(CYAN) _____ ______ ______  _____    ___   _____ __   __ _____  _____ \n$(RESET)"
	@printf "$(CYAN)/  __ \| ___ \| ___ \|  _  |  /   | |  ___|\ \ / /|  _  ||  _  |\n$(RESET)"
	@printf "$(CYAN)| /  \/| |_/ /| |_/ /| |/' | / /| | | |__   \ V / | |/' || |/' |\n$(RESET)"
	@printf "$(CYAN)| |    |  __/ |  __/ |  /| |/ /_| | |  __|  /   \ |  /| ||  /| |\n$(RESET)"
	@printf "$(CYAN)| \__/\| |    | |    \ |_/ /\___  | | |___ / /^\ \\ |_/ /\ |_/ /\n$(RESET)"
	@printf "$(CYAN) \____/\_|    \_|     \___/     |_/ \____/ \/   \/ \___/  \___/ \n$(RESET)"
	@printf "\n"



$(OBJ_DIR)%.o:$(SRC_DIR)%.cpp
	@mkdir -p $(OBJ_DIR)
	@echo "$(CYAN)Compiling...        [$@]$(RESET)"
	@$(CC) $(FLAGS) -o $@ -c $<
	@printf "$(UP)$(CUT)"


clean:
	@if [ -d "$(OBJ_DIR)" ]; then \
	rm -rf $(OBJ_DIR); \
	echo "$(PURPLE)Delete all objects  [$(NAME)]$(RESET)"; else \
	echo "$(YELLOW)No object to remove [$(NAME)]$(RESET)"; \
	fi;

fclean: clean
	@if [ -f "$(NAME)" ]; then \
	rm -rf $(NAME); \
	echo "$(PURPLE)Delete output file  [$(NAME)]$(RESET)"; else \
	echo "$(YELLOW)No output to remove [$(NAME)]$(RESET)"; \
	fi;

re:	fclean all

.PHONY:	all clean fclean re
