NAME = libftprintf.a

SRCS = $(wildcard ft*.c)

OBJS = $(SRCS:.c=.o)

all: $(NAME)

$(NAME): $(OBJS)
	@ar -rcs $(NAME) $^

%.o: %.c
	@gcc -Wall -Wextra -Werror -o $@ -c $^

clean:
	@rm -rf *.o

test: $(NAME)
	@gcc $^ test.c
	@./a.out
	@rm ./a.out

fclean: clean
	@rm -rf $(NAME)

re: $(NAME) fclean
	make fclean
	make


.PHONY: re fclean clean all