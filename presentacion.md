!SLIDE

# RSpec

!SLIDE 

@@@ ruby
    class TestSimpleNumber < Test::Unit::TestCase
     
      def test_add
        assert_equal(4, SimpleNumber.new(2).add(2) )
      end
     
      def test_multiply
        assert_equal(6, SimpleNumber.new(2).multiply(3) )
      end

    end
@@@


!SLIDE 

@@@ ruby
    describe SimpleNumber do
     
      it "should add numbers" do
        SimpleNumber.new(2).add(2).should eql 4
      end
      
      it "should multiply numbers" do
        SimpleNumber.new(2).multiply(3).should eql 6
      end
     
    end
@@@

!SLIDE

@@@ ruby
    def test_add
      assert_equal(4, SimpleNumber.new(2).add(2) )
      assert_equal(0, SimpleNumber.new(2).add(-2) )
      assert_equal(0, SimpleNumber.new(-2).add(2) )
      assert_equal(-4, SimpleNumber.new(-2).add(-2) )
    end
@@@

!SLIDE
@@@ ruby
    it "should add + and - negative numbers" do
      SimpleNumber.new(2).add(-2).should eql 0
      SimpleNumber.new(-2).add(2).should eql 0
    end

    it "should add - numbers" do
      SimpleNumber.new(-2).add(-2).should eql -4
    end
@@@

!SLIDE

@@@ ruby
    my_list.should have(3).items
    lambda {my_list << 3}.should change(my_list, :lenght).by(1)
    lambda {my_list.not_defined_method}.should raise_error
    [2, 3, 1].should =~ [3, 1, 2]
@@@

!SLIDE

# Dudas?

