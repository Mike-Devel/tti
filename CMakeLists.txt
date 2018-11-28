# Copyright 2018 Mike Dev
# Distributed under the Boost Software License, Version 1.0.
# See accompanying file LICENSE_1_0.txt or copy at http://www.boost.org/LICENSE_1_0.txt

cmake_minimum_required(VERSION 3.5)
project(BoostTti LANGUAGES CXX)

add_library(boost_tti INTERFACE)
add_library(Boost::tti ALIAS boost_tti)

target_include_directories(boost_tti INTERFACE include)

target_link_libraries(boost_tti
    INTERFACE
        Boost::config
		Boost::function_types
		Boost::mpl
		Boost::preprocessor
		Boost::type_traits
)
