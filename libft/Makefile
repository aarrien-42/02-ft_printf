# Normbre del ejecutable
NAME = libft.a

# Colores
NC = \033[0m
BLACK = \033[0;30m
RED = \033[0;31m
GREEN = \033[0;32m
YELLOW = \033[0;33m
BLUE = \033[0;34m
PURPLE = \033[0;35m
CYAN = \033[0;36m
WHITE = \033[0;37m

# Directorios
SRC_DIR = srcs/
OBJ_DIR = objs/
OBJF = objs
INC = ../incs

# Ficheros
SRC_IS = ft_isalnum ft_isalpha ft_isascii ft_isdigit ft_isprint
SRC_LST = ft_lstadd_back_bonus ft_lstadd_front_bonus ft_lstclear_bonus ft_lstdelone_bonus \
			ft_lstiter_bonus ft_lstlast_bonus ft_lstmap_bonus ft_lstnew_bonus ft_lstsize_bonus
SRC_MEM = ft_bzero ft_calloc ft_memchr ft_memcmp ft_memmove ft_memset
SRC_PUT = ft_putchar_fd ft_putendl_fd ft_putnbr_fd ft_putstr_fd
SRC_STR = ft_split ft_strchr ft_strdup ft_striteri ft_strjoin \
			ft_strlcat ft_strlcpy ft_strlen ft_strmapi ft_strncmp \
			ft_strnstr ft_strrchr ft_strtrim ft_substr
SRC_TO = ft_atoi ft_itoa ft_tolower ft_toupper

SRC_FILES = $(SRC_IS) $(SRC_LST) $(SRC_MEM) $(SRC_PUT) $(SRC_STR) $(SRC_TO)
SRC = $(addprefix $(SRC_DIR), $(addsuffix .c, $(SRC_FILES)))
OBJ = $(addprefix $(OBJ_DIR), $(addsuffix .o, $(SRC_FILES)))

# Comandos
CC = gcc
CFLAGS = -Wall -Werror -Wextra
RM = rm -f
AR = ar rcs

# REGLAS #
all: $(NAME)

$(NAME): $(OBJ)
	@$(AR) $(NAME) $(OBJ)

$(OBJ_DIR)%.o: $(SRC_DIR)%.c | $(OBJF)
	printf "$(BLUE)Compiling: $< $(NC)"
	@$(CC) $(CFLAGS) -I $(INC) -c $< -o $@
	echo "$(GREEN) Done! $(NC)"

$(OBJF):
	@mkdir -p $(OBJ_DIR)

clean:
	@$(RM) -r $(OBJ_DIR)

fclean: clean
	@$(RM) $(NAME)

re: fclean all

.PHONY: all clean fclean re
