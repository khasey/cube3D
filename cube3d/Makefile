# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: kthierry <kthierry@student.42.fr>          +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2022/11/23 01:28:05 by kthierry          #+#    #+#              #
#    Updated: 2022/11/23 02:57:05 by kthierry         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

NAME = cube3D
SRC = srcs

NONE := '\033[0m'
GREEN := '\033[92m'
GRAY := '\033[90m'
RED := '\033[91m'
CURSIVE := '\033[3m'

SRCS =	$(wildcard $(SRC)/*.c)

OBJ=$(SRCS:.c=.o)

%.o: %.c
	$(CC) -Wall -Wextra -Werror -Imlx -c $< -o $@

$(NAME): $(OBJ)
	@echo $(CURSIVE)$(GREEN)"-- Making $(NAME) --"$(NONE)
	$(CC) $(OBJ) -lmlx -framework OpenGL -framework AppKit -o $(NAME)
	@echo $(GREEN)$ "--$(NAME) was created --"$(NONE)
all:
	$(MAKE) $(NAME)

clean:
	@echo $(CURSIVE)$()" -- Deleting objects --"$(NONE)
	rm -f $(OBJ) 
	@echo $(RED)"--objects was deleted -- "$(NONE)

fclean: clean
	@echo $(CURSIVE)$(RED)"-- Deleting $(NAME) --"$(NONE)
	rm -f $(NAME) 
	@echo $(RED)"-- $(NAME) was deleted -- "$(NONE)

re: fclean all