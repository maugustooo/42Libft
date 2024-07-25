# libft

First library for school 42. Always updating.

## PART 1

### Replicas of <ctype.h>

Function | Format | Description
--- | --- | --- 
ft_isalpha | `int	ft_isalpha(int c)` | Check if character c (int format) is alphabetic 
ft_isdigit | `int	ft_isdigit(int c)` | Check if character c (int format) is numeric
ft_isalnum | `int	ft_isalnum(int c)` | Check if character c (int format) is alphanumeric
ft_isascii | `int	ft_isascii(int c)` | Check if character c (int format) is ASCII 
ft_isprint | `int	ft_isprint(int c)` | Check if character c (int format) is printable 
ft_toupper | `int	ft_toupper(int c)` | If c is a lowercase letter, returns its uppercase equivalent
ft_tolower | `int	ft_tolower(int c)` | If c is an uppercase letter, returns its lowercase equivalent 
ft_strlen | `size_t	ft_strlen(const char *str)` | Checks number of characters in string str 
ft_memset | `void	*ft_memset(void *s, int c, size_t n)` | Fills the first n bytes of the memory area pointed to by s with the constant byte c
ft_bzero | `void	ft_bzero(void *s, size_t n)` | Erases the first n bytes of memory in memory area pointed to by s 
ft_strlcpy | `size_t	ft_strlcpy(char *dest, const char *src, size_t size)` | Copy "size" bytes from src to dst 
ft_memcpy | `void	*ft_memcpy(void *dest, const void *src, size_t n)` | Copy n bytes of memory from src to dest. There is risk of memory overlap 
ft_memmove | `void	*ft_memmove(void *dest, const void *src, size_t n)` | Copy n bytes of memory from src to dest. Avoids memory overlap
ft_strlcat | `size_t	ft_strlcat(char *dest, const char *src, size_t size)` | Concatenate src into dest. Final string will have "size" bytes 
ft_strchr | `char	*ft_strchr(const char *str, int c)` | Returns pointer to first instance of char c in str 
ft_strrchr | `char	*ft_strrchr(const char *str, int c)` | Returns pointer to last instance of char c in str
ft_memchr | `void	*ft_memchr(const void *str, int c, size_t n)` | Returns pointer to first instance of char c in str. Only checks the first n bytes 
ft_strncmp | `int	ft_strncmp(const char *s1, const char *s2, size_t n)` | Compare the first n bytes of strings s1 and s2
ft_memcmp | `int	ft_memcmp(const void *s1, const void *s2, size_t n)` | Compare the first n bytes of variables s1 and s2 
ft_strnstr | `char	*ft_strnstr(const char *big, const char *little, size_t len)` | Checks if string little exists in string big, within len characters
ft_strdup | `char	*ft_strdup(const char *src)` | Creates new string as a duplicate of src [requires malloc]
ft_atoi | `int	ft_atoi(const char *str)` | Converts written number from a string str into int format
ft_calloc | `void	*ft_calloc(size_t nmemb, size_t size)` | Allocates memory to an array of nmemb elements of "size" bytes each. [requires malloc]

## PART 2

Function | Format | Description
--- | --- | ---
ft_substr | `char	*ft_substr(const char *str, unsigned int start, size_t len)` | Creates new string, equivalent to a pointer to str at the "start" location. len is maximum size. [requires malloc]
ft_strjoin | `char	*ft_strjoin(const char *s1, const char *s2)` | Concatenates s1 and s2 into a new string. [requires malloc]
ft_strtrim | `char	*ft_strtrim(const char *s1, const char *set)` | Trims beginning and end of string s1 out of all "set" characters. [requires malloc] 
ft_split | `char	**ft_split(const char *s, char c)` | Divides string s into words (delimited by c), and turns each word into a string. [requires malloc & free]
ft_itoa | `char	*ft_itoa(int n)` | Converts a number into a string. [requires malloc]
ft_strmapi | `char	*ft_strmapi(const char *str, char (*f)(unsigned int, char))` | Applies function f to each character of str, returning a string with the results. [requires malloc]
ft_striteri | `void	ft_striteri(char *str, void (*f)(unsigned int, char))` | Applies function f to each character of str, altering str in the process 
ft_putchar_fd | `void	ft_putchar_fd(char c, int fd)` | Prints c to the file descriptor fd. [requires write] 
ft_putstr_fd | `void	ft_putstr_fd(char *str, int fd)` | Prints str to the file descriptor fd. [requires write] 
ft_putendl_fd | `void	ft_putendl_fd(char *str, int fd)` | Prints str to the file descriptor fd, followed by a newline. [requires write] 
ft_putnbr_fd | `void	ft_putnbr_fd(int n, int fd)` | Prints n to the file descriptor fd. [requires write] 

## BONUS

Function | Format | Description
--- | --- | --- 
ft_lstnew | `t_list	*ft_lstnew(void *content)` | Creates new node with "content". "next" node becomes NULL. [requires malloc] 
ft_lstadd_front | `void	 ft_lstadd_front(t_list **lst, t_list *new)` | Adds node "new" to the front of the lst
ft_lstsize | `int	 ft_lstsize(t_list *lst)` | Checks number of nodes in lst
ft_lstlast | `t_list	 *ft_lstlast(t_list *lst)` | Checks last node in lst
ft_lstadd_back | `void	 ft_lstadd_back(t_list **lst, t_list *new)` | Adds node "new" to the back of the lst 
ft_lstdelone | `void	 ft_lstdelone(t_list *lst, void (*del)(void *))` | Frees memory from current node's content in lst, using the del function. [requires free]
ft_lstclear | `void	 ft_lstclear(t_list **lst, void (*del)(void *))` | Frees memory from current node's content in lst, as well as all following nodes, using the del function. List then points to NULL. [requires free]
ft_lstiter | `void	 ft_lstiter(t_list *lst, void (*f)(void *))` | Applies function f to each node in lst
ft_lstmap | `t_list	 *ft_lstmap(t_list *lst, void *(*f)(void *), void (*del)(void *))` | Applies function f to each node in lst, returning a new list with the results. Node content is freed with del wherever necessary. [requires malloc & free] 
## Later Additions
# libft

## Later Additions

Function | Format | Description | Return
--- | --- | --- | ---
ft_printf | `int	ft_printf(const char *string, ...)` | Prints a string, converting a series of variables according to a specific cipher [requires va_ functions] | Printed length
get_next_line | `char	*get_next_line(int fd)` | This function returns a line that can be read from fd. Successive uses return the following lines. | The next line
