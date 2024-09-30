```Table dim_books {
  book_id string [pk]
  title string
  price float //it's always the same for the same book
}

Table dim_users {
  user_id string [pk]
  username string //it's always unique
}

Table fact_reviews {
  review_id string [pk]
  book_id string [ref: > dim_books.book_id]
  user_id string [ref: > dim_users.user_id]
  review_helpfulness string
  review_score int
  review_time int
  review_summary string
  review_text string
}```