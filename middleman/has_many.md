# How to manage a has_many relaction with Dato

If you have with Dato:

    author > has_many > books
    book > belengs_to > author

You can loop each all books in author view in this way:

    dato.books.select { |b| b.authors.include?(author) }.each do |book|
