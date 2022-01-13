require 'csv'

desc "output each row of a csv as a text file"
task :csv_to_txt do 
    CSV.foreach(("_data/state-of-the-union/csv/sotu_20th_century.csv"), headers: true, col_sep: ",") do |row|
        filename = row["id"]
        newdoc = File.new("_data/state-of-the-union/txt/" + filename + ".txt", 'w')
        newdoc << row["text"]
        newdoc.close
    end
end